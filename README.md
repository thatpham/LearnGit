https://social.msdn.microsoft.com/Forums/vstudio/en-US/4d842747-7d6d-4e97-adc4-fa4f9e904856/check-halfsize-and-fullsize-kanji-characters-and-katakana-characters?forum=vbgeneral
https://stackoverflow.com/questions/19919439/c-convert-japanese-text-encoding-in-shift-jis-and-stored-as-ascii-into-utf-8
public static void Main()
	{
		var badstringFromDatabase = "使";
        var recovered1 = System.Text.Encoding.GetEncoding(932).GetBytes(badstringFromDatabase); //Shift JIS
		Console.WriteLine("byte Shift JIS:"+recovered1.Length);
        Console.WriteLine("Shift JIS: " + System.Text.Encoding.GetEncoding(932).GetString(recovered1)); //Shift JIS

	}
