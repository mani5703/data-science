# data-science
import bs4 as bs
import urllib.request as url_x
import pandas as pd
BusinesNames=[]
Phone=[]


url = "https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA"

urlsource=''+url+'&start='
no_of_pages=5
for iteration in range(no_of_pages):
  s=iteration*10
  if(s==0):
    s=1
  source = url_x.urlopen(urlsource+str(s))
  print(urlsource+str(s))

  page_soup = bs.BeautifulSoup(source, 'html.parser')

  mains = page_soup.find_all("span", {"class": " css-1pxmz4g"})
  for main in mains:
      try:
          busname = main.find("a", {"class" : "css-166la90"}).text
          BusinesNames.append(busname)
      except:
          print("Information not provided")
  print('Loading......')
print('Done with processing...')
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=10
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=20
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=30
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
Done with processing...
[ ]
BusinesNames

['Fable',
 'Marufuku Ramen SF',
 'Farmhouse Kitchen Thai Cuisine',
 'Starbelly',
 'Sweet Maple',
 'Jaranita',
 'Beretta',
 'Nopa',
 'The Snug',
 'Fog Harbor Fish House',
 'Nopalito',
 'Marufuku Ramen SF',
 'Che Fico Alimentari',
 'Horsefeather',

[ ]
import bs4 as bs
import urllib.request as url_x
import pandas as pd
[3]
BusinesNames=[]
Phone=[]


url = "https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA"

urlsource=''+url+'&start='
[ ]
no_of_pages=5
for iteration in range(no_of_pages):
  s=iteration*10
  if(s==0):
    s=1
  source = url_x.urlopen(urlsource+str(s))
  print(urlsource+str(s))

  page_soup = bs.BeautifulSoup(source, 'html.parser')

  mains = page_soup.find_all("span", {"class": " css-1pxmz4g"})
  for main in mains:
      try:
          busname = main.find("a", {"class" : "css-166la90"}).text
          BusinesNames.append(busname)
      except:
          print("Information not provided")
  print('Loading......')
print('Done with processing...')

https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=1
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=10
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=20
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=30
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
https://www.yelp.com/search?cflt=restaurants&find_loc=San+Francisco%2C+CA&start=40
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Information not provided
Loading......
Done with processing...
[ ]
BusinesNames

['Fable',
 'Marufuku Ramen SF',
 'Farmhouse Kitchen Thai Cuisine',
 'Starbelly',
 'Sweet Maple',
 'Jaranita',
 'Beretta',
 'Nopa',
 'The Snug',
 'Fog Harbor Fish House',
 'Nopalito',
 'Marufuku Ramen SF',
 'Che Fico Alimentari',
 'Horsefeather',
 'a Mano',
 'The Snug',
 'The Front Porch',
 'Ragazza',
 'Farmhouse Express',
 'Parada 22',
 'Cha Cha Cha',
 'Konomama',
 'Beit Rima',
 'Brenda’s French Soul Food',
 'Blind Butcher',
 'Willkommen',
 'Jaranita',
 'Katsuya',
 'Um Ma',
 'Padrecito',
 'Brenda’s French Soul Food',
 'Brenda’s Meat & Three',
 'AshYan’s Lu Ruo Fan',
 'Presidio Kebab',
 'Anchor Oyster Bar',
 'Dumpling House',
 'Yama-chan',
 'State Bird Provisions',
 'Pearl 6101',
 'Hotbird',
 'Katsuya',
 'Willkommen',
 'Loló',
 'Bhoga',
 'Tacos El Patrón',
 'Farmhouse Express',
 'Fog Harbor Fish House',
 'L’Ardoise Bistro',
 'Voodoo Love',
 'Souvla']
[ ]
Phone

[]
[ ]
dictionary = {'BusinessNames': BusinessNames, 'Phone': Phone} 


amul=pd.DataFrame(dict([(k,pd.Series(v)) for k,v in dictionary.items()]))
[ ]
amul

