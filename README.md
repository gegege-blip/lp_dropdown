# lp_dropdown

import flet as ft




def main(page: ft.Page):


    cor = ft.Text(value='Botão que muda de cor')
    def change_color(e):
        selected_color = {
            "Red": ft.colors.RED_200,
            "Purple": ft.colors.PURPLE_200,
            "Blue": ft.colors.BLUE_200}.get(e.control.value, ft.colors.WHITE)
        d.bgcolor = selected_color
        d.color= ft.colors.BLACK
        page.update()


    d = ft.Dropdown(
        label= 'Opções',
        width= 1000,
        options=[
            ft.dropdown.Option("Red"),
            ft.dropdown.Option("Purple"),
            ft.dropdown.Option("Blue"),
        ],
        on_change=change_color,
        border_color= ft.colors.PINK_500)


    page.add(cor, d)



    def button_clicked(e):

        t.value = f"Você escolheu {dd.value}"
        page.update()


    p = ft.Text(value='Botão com on click')


    t = ft.Text()
    b = ft.ElevatedButton(text="Submit", on_click=button_clicked)
    dd = ft.Dropdown(
        label= 'Opções',
        width= 1000,
        options=[
            ft.dropdown.Option("Red"),
            ft.dropdown.Option("Purple"),
            ft.dropdown.Option("Blue"),
        ],
        border_color= ft.colors.BLUE_600)


    page.add(p, dd, t, b)


ft.app(main)



