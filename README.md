# projecttodolist
Projekts Python valodā: Datu struktūras un algoritmi

Uzdevums: Izstrādāt programmu ar uzdevumu pierakstes funkcionalitāti (To do list). Programmai ir ātri jāpievieno, jāizdzēš uzdevumu un laiku līdz kuram jāpabeidz, ir jābūt iespējai saglabāt izveidoto sarakstu excel failā. Tomēr programma nevar filtrēt uzdevumus, tikai izvadīt tos pēc pievienošanas kārtas. Lai filtrētu datus ir ideja izmantot min Heap, izmantojot laiku kā skaitlu (piemēram, 23:30 ir 2330 ir mazāks nekā 23:35 kas ir 2335 - uzdevums ir pirmais izpildīšanai.) Un ja pievienot uzdevumus pēc kārtas tas nebūs līdzīgs sarakstam (kā bināram kokam BST). Tomēr kodā tiek izmantota vārdnīca, jo galvenais uzdevums "to do" sarakstam ir ātri pievienot, dzēst un atrast kad izpildīt uzdevumu. Visu to dictionary dara 0(1) pēc laika. Bet izmantojot min Heap pievienošana aizņems 0(log n) kas ir mazliet lēnāks nekā dictionary, tomēr dzēšana aizņems O(n + log n) (n atrašanai un log n dzēšanai), kas nebūs efektīvi. 

Python bibliotēkas: ir izmantota openpyxl bibliotēka, importēta Workbbook jauna faila izstrādei un load_workbook lai lasītu jau izveidotu failu.

Metodes:
Load(): ielādē datus no excel faila.
Save_file(): saglabā excel failu ar kollonām Uzdevumi un Laiks
add_task(): pievieno tikai uzdevumu un saglabā to
add_time(): pievieno tikai laiku un saglabā to
add_both(): pievieno uzdevumu un laiku un saglabā. Izmanto convert()
convert(time): sanem laiku formātā stundas:minūtes, un dala tos uz minūtēm un sekundēm. Strādā, ja stundu skaits ir lielāks par 0 un mazāks vai vienāds ar 23, un stundu skaits ir lielāks par 0 un mazāks vai vienāds ar 59.
remove_task(): izdzēš uzdevumu ja tāds ir un saglabā izmaiņas.
print_tasks(): izvada uzdevumus
print_both(): izvada uzdevumu un laiku pēc kārtas.
main(): piedāvā izvēlēties komandu: add / del / see / out. Pēc out izvēles komanda apstājas
