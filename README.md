# Hangman-
   # игра виселица
    повесить  = []
    повесить . добавить ( ' +---+' )
    повесить . добавить ( ' | |' )
    повесить . добавить ( ' |' )
    повесить . добавить ( ' |' )
    повесить . добавить ( ' |' )
    повесить . добавить ( ' |' )
    повесить . добавить ( '=======' )
    
    мужчина  = {}
    человек [ 0 ] = [ '0 |' ]
    человек [ 1 ] = [ '0 |' , ' | |' ]
    человек [ 2 ] = [ '0 |' , '/| |' ]
    человек [ 3 ] = [ '0 |' , '/| \\   |' ]
    человек [ 4 ] = [ '0 |' , '/| \\   |' , '/ |' ]
    человек [ 5 ] = [ '0 |' , '/| \\   |' , '/ \\   |' ]
    
    фото  = []
    
    слова  =  '''муравей бабуин барсук летучая мышь медведь бобр верблюд кошка моллюск кобра пума койот
ворона олень собака осел утка орел хорек лиса лягушка коза гусь ястреб лев ящерица лама
крот обезьяна лось мышь мул тритон выдра сова панда попугай голубь питон кролик баран
крыса ворон носорог лосось морская акула овца скунс ленивец змея паук аист лебедь тигр
жаба форель индейка черепаха ласка кит волк вомбат зебра''' . разделить ()

    infStr = '_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' *-_-* \' '
  
    def  __init__ ( self , * args , ** kwargs ):
        я , j  =  2 , 0
        сам . фото . добавить ( сам . повесить [:])
        для  ls  в  себе . мужчина . значения ():
            рис , j  =  сам . повесить [:], 0
            для  м  в  лс :
                рис [ я  +  j ] =  м
                j  +=  1
            сам . фото . добавить ( рис. )
def  pickWord ( сам ):
        вернуть  себя . слова [ случайный . randint ( 0 , len ( сам . слова ) -  1 )]
    
    def  printPic ( self , idx , wordLen ):
        для  строки  в  себя . фото [ idx ]:
            печать ( строка )
            
    def  askAndEvaluate ( я , слово , результат , пропущено ):
        предположение  =  ввод ()
        если  угадать  ==  Нет  или  len ( угадать ) !=  1  или ( угадать  в  результате ) или ( угадать  в  пропущенном ):
            вернуть  Нет , Ложь
        я  =  0
        правильно  =  угадать  в  слове
        для  c  в  слове :
            если  c  ==  угадать :
                результат [ я ] =  с
            я  +=  1
        вернуть  предположение , право

    деф  информация ( я , информация ):
        ln = len ( сам . infStr )
        печать ( сам .infStr [ : - 3 ])
        печать ( информация )
        печать ( сам . infStr [ 3 :])
            
    деф  старт ( сам ):
        print ( «Добро пожаловать в Виселицу!» )
        слово  =  список ( сам . pickWord ())
        результат  =  список ( '*'  *  длина ( слово ))
        print ( 'Слово:' , результат )
        успех , я , пропущено  =  Ложь , 0 , []
        в то время как  я  <  len ( селф . фото ) - 1 :
            print ( 'Угадай слово:' , end = '' )
            думаю , правильно  =  сам . askAndEvaluate ( слово , результат , пропущено )
            если  предположить  ==  Нет :
                print ( 'Вы уже вводили этот символ. ' )
                Продолжать
            print ( '' . присоединиться ( результат ))
            если  результат  ==  слово :
                сам . info ( ' Поздравляем! Вы только что спасли жизнь!' )
                успех  =  Истина
                перерыв
            если  не  прав :
                пропустил . добавить ( угадать )
                я += 1
            сам . printPic ( i , len ( слово ))
            print ( 'Пропущенные символы:' , пропущено )
        
        если  не  успех :
            сам . info ( 'Слово было \' ' + '' . join ( слово ) + ' \' ! Ты только что убил человека, йо !' )

а  =  Виселица (). начать ()
