# adicionar-novo-local-armazenamento-steam
Adicionar um novo local de armazenamento dos jogos no Steam

Este manual explica como adicionar um novo local de armazenamento para os seus jogos no Steam, pois até o momento, a plataforma só nos permite adicionar um local de armazenamento por unidade, e as vezes queremos centralizar todos os nossos jogos em apenas um local.

1. Abra o arquivo: C:\Program Files (x86)\Steam\config\libraryfolders.vdf
2. Abra o arquivo C:\Program Files (x86)\Steam\config\libraryfolders.vdf

Observe que o conteúdo dos dois arquivos são identicos. Por exemplo:

```

"libraryfolders"
{
    "0"
    {
 	   "path"		"C:\\Program Files (x86)\\Steam"
 	   "label"		""
 	   "contentid"		"1234567891234567891"
 	   "totalsize"		"0"
 	   "update_clean_bytes_tally"		"0"
 	   "time_last_update_corruption"		"0"
 	   "apps"
 	   {
 	   }
    }
}

```

 Você precisará adicionar um novo bloco de código antes do último colchete no final do bloco de ambos os arquivos e salvá-los. Faça isso com o Steam totalmente fechado. Apenas minimizar o aplicativo não basta.

 3. Adicione o seguinte bloco antes do último colchete:

```

"1"
{
    "path"          "C:\\Games\\Steam"
}

```

Editando corretamente o seu arquivo ficará parecido com esse:

```

"libraryfolders"
{
	"0"
	{
		"path"		"C:\\Program Files (x86)\\Steam"
		"label"		""
		"contentid"		"1234567891234567891"
		"totalsize"		"0"
		"update_clean_bytes_tally"		"0"
		"time_last_update_corruption"		"0"
		"apps"
		{
		}
	}
	"1"
	{
		"path"		"C:\\Games\\Steam"
	}
}

```

Pronto! Agora você poderá instalar seus jogos em outra pasta.

Observe que no momento da instalação de qualquer jogo, o Steam deverá sugerir dois "Disco local (C:)" para instalar o jogo, o último será a nova localização.
