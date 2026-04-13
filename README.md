# C-authorization-
   private void btnLogin_Click(object sender, RoutedEventArgs e)
        {
            string login = tbLogin.Text;
            string password = pbPassword.Password;

            string[,] users =
            {
                { "admin", "123" },
                { "user", "111" },
                { "student", "qwerty" }
            };

            bool ok = false;

            for (int i = 0; i < users.GetLength(0); i++)
            {
                if (login == users[i, 0] && password == users[i, 1])
                {
                    ok = true;
                    break;
                }
            }

            if (ok)
                MessageBox.Show("Авторизация успешна");
            else
                MessageBox.Show("Неверный логин или пароль");
        }
    }
}