
вывод данных из бд 2. представление плиткой(часто одна страница под каждый вывод) 3. за таблицу отвечает grid, за плитку - listView Алгоритм: для получения данных нужно создать context

public static OOORulEntities context;

    public static OOORulEntities getcontext()
    {
        if (context == null)
        {
            context = new Models.OOORulEntities();
        }
        return context;
    }
вторая строка для кнопок добавить и удалить 4. данные из таблицы - DataGrid имя обычно включает DataGrid и имя таблицы 5. создаем столбцы: <DataGrid.Columns> <DataGridTemplateColumn.CellTemplate> </DataGridTemplateColumn.CellTemplate> </DataGrid.Columns>

    </DataGrid>

    6. структура столбца: заголовок (предпочтительно на русском), указание на столбец таблицы, ширина (Header="Пароль" Binding="{Binding Password}"  Width="auto")
    7. Вывод данных: название DataGrid, эелементы, равно, БД, getContext(), название таблицы, функция ToList()
 
       DGUsers.ItemsSource = Models.OOORulEntities.getcontext().Datas.ToList();
#CRUD Create update delete - создание редактирование удаление
