---
UID: NF:stringapiset.MultiByteToWideChar
title: MultiByteToWideChar function (stringapiset.h)
description: Maps a character string to a UTF-16 (wide character) string.
helpviewer_keywords: ["CP_ACP","CP_MACCP","CP_OEMCP","CP_SYMBOL","CP_THREAD_ACP","CP_UTF7","CP_UTF8","MB_COMPOSITE","MB_ERR_INVALID_CHARS","MB_PRECOMPOSED","MB_USEGLYPHCHARS","MultiByteToWideChar","MultiByteToWideChar function [Internationalization for Windows Applications]","_win32_MultiByteToWideChar","intl.multibytetowidechar","stringapiset/MultiByteToWideChar"]
old-location: intl\multibytetowidechar.htm
tech.root: Intl
ms.assetid: a117fdfe-b52b-466f-9300-6455e91ea2a8
ms.date: 02/05/2024
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_SYMBOL, CP_THREAD_ACP, CP_UTF7, CP_UTF8, MB_COMPOSITE, MB_ERR_INVALID_CHARS, MB_PRECOMPOSED, MB_USEGLYPHCHARS, MultiByteToWideChar, MultiByteToWideChar function [Internationalization for Windows Applications], _win32_MultiByteToWideChar, intl.multibytetowidechar, stringapiset/MultiByteToWideChar
req.header: stringapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - MultiByteToWideChar
 - stringapiset/MultiByteToWideChar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - vertdll.dll
api_name:
 - MultiByteToWideChar
---

# MultiByteToWideChar function

## -description

Maps a character string to a UTF-16 (wide character) string. The character string is not necessarily from a multibyte character set.

## -parameters

### -param CodePage [in]

Code page to use in performing the conversion. This parameter can be set to the value of any code page that is installed or available in the operating system. For a list of code pages, see [Code Page Identifiers](/windows/win32/Intl/code-page-identifiers). Your application can also specify one of the values shown in the following table.

| Value                | Meaning |
|----------------------|---------|
| **CP_ACP**           | The system default Windows ANSI code page.<br><br>**Note:** This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible. |
| **CP_MACCP**         | The current system Macintosh code page (used primarily in legacy code and is typically not needed as Macintosh computers use Unicode for encoding.).<br><br>**Note:** This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible. |
| **CP_OEMCP**         | The current system OEM code page.<br><br>**Note:** This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible. |
| **CP_SYMBOL**        | Symbol code page (42). |
| **CP_THREAD_ACP**    | The Windows ANSI code page for the current thread.<br><br>**Note:** This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible. |
| **CP_UTF7**          | UTF-7. Use this value only when forced by a 7-bit transport mechanism. Use of UTF-8 is preferred. |
| **CP_UTF8**          | UTF-8. |

### -param dwFlags [in]

Flags indicating the conversion type. The application can specify a combination of the following values, with MB_PRECOMPOSED being the default. MB_PRECOMPOSED and MB_COMPOSITE are mutually exclusive. MB_USEGLYPHCHARS and MB_ERR_INVALID_CHARS can be set regardless of the state of the other flags.

| Value | Meaning |
|-------|---------|
| **MB_COMPOSITE** | Always use decomposed characters, that is, characters in which a base character and one or more nonspacing characters each have distinct code point values. For example, Ä is represented by A + ¨: LATIN CAPITAL LETTER A (U+0041) + COMBINING DIAERESIS (U+0308). Note that this flag cannot be used with MB_PRECOMPOSED. |
| **MB_ERR_INVALID_CHARS** | Fail if an invalid input character is encountered.<br/><br/>Starting with Windows Vista, the function does not drop illegal code points if the application does not set this flag, but instead replaces illegal sequences with U+FFFD (encoded as appropriate for the specified codepage).<br/><br/>**Windows 2000 with SP4 and later, Windows XP:** If this flag is not set, the function silently drops illegal code points. A call to [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns ERROR_NO_UNICODE_TRANSLATION. |
| **MB_PRECOMPOSED** | Default; do not use with MB_COMPOSITE. Always use precomposed characters, that is, characters having a single character value for a base or nonspacing character combination. For example, in the character è, the e is the base character and the accent grave mark is the nonspacing character. If a single Unicode code point is defined for a character, the application should use it instead of a separate base character and a nonspacing character. For example, Ä is represented by the single Unicode code point LATIN CAPITAL LETTER A WITH DIAERESIS (U+00C4). |
| **MB_USEGLYPHCHARS** | Use glyph characters instead of control characters. |

For the code pages listed below, *dwFlags* must be set to `0`. Otherwise, the function fails with **ERROR_INVALID_FLAGS**.

- 50220
- 50221
- 50222
- 50225
- 50227
- 50229
- 57002 through 57011
- 65000 (UTF-7)
- 42 (Symbol)

> [!NOTE]
> For UTF-8 or code page 54936 (GB18030, starting with Windows Vista), *dwFlags* must be set to either `0` or **MB_ERR_INVALID_CHARS**. Otherwise, the function fails with **ERROR_INVALID_FLAGS**.

### -param lpMultiByteStr [in]

Pointer to the character string to convert.

### -param cbMultiByte [in]

Size, in bytes, of the string indicated by the *lpMultiByteStr* parameter. Alternatively, this parameter can be set to -1 if the string is null-terminated. Note that, if *cbMultiByte* is `0`, the function fails.

If this parameter is -1, the function processes the entire input string, including the terminating null character. Therefore, the resulting Unicode string has a terminating null character, and the length returned by the function includes this character.

If this parameter is set to a positive integer, the function processes exactly the specified number of bytes. If the provided size does not include a terminating null character, the resulting Unicode string is not null-terminated, and the returned length does not include this character.

### -param lpWideCharStr [out, optional]

Pointer to a buffer that receives the converted string.

### -param cchWideChar [in]

Size, in characters, of the buffer indicated by *lpWideCharStr*. If this value is `0`, the function returns the required buffer size, in characters, including any terminating null character, and makes no use of the *lpWideCharStr* buffer.

## -returns

Returns the number of characters written to the buffer indicated by *lpWideCharStr* if successful. If the function succeeds and *cchWideChar* is `0`, the return value is the required size, in characters, for the buffer indicated by *lpWideCharStr*. Also see *dwFlags* for info about how the **MB_ERR_INVALID_CHARS** flag affects the return value when invalid sequences are input.

The function returns `0` if it does not succeed. To get extended error information, the application can call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md), which can return one of the following error codes:

- **ERROR_INSUFFICIENT_BUFFER**:  A supplied buffer size was not large enough, or it was incorrectly set to `NULL`.
- **ERROR_INVALID_FLAGS**: The values supplied for flags were not valid.
- **ERROR_INVALID_PARAMETER**: Any of the parameter values was invalid.
- **ERROR_NO_UNICODE_TRANSLATION**: Invalid Unicode was found in a string.

## -remarks

The default behavior of this function is to translate to a precomposed form of the input character string. If a precomposed form does not exist, the function attempts to translate to a composite form.

> [!WARNING]
> Using **MultiByteToWideChar** incorrectly can compromise the security of your application. Calling this function can easily cause a buffer overrun because the size of the input buffer indicated by *lpMultiByteStr* equals the number of bytes in the string, while the size of the output buffer indicated by *lpWideCharStr* equals the number of characters. To avoid a buffer overrun, your application must specify a buffer size appropriate for the data type the buffer receives. For more information, see <a href="/windows/win32/Intl/security-considerations--international-features">Security Considerations: International Features</a>.

The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use Unicode, such as UTF-8 or UTF-16, instead of a specific code page, unless legacy standards or data formats prevent the use of Unicode. If using Unicode is not possible, applications should tag the data stream with the appropriate encoding name when protocols allow it. HTML and XML files allow tagging, but text files do not.

The output buffer can easily be overrun if this function is not first called with *cchWideChar* set to `0` in order to obtain the required size. If the MB_COMPOSITE flag is used, the output can be three or more characters long for each input character.

The use of the MB_PRECOMPOSED flag has very little effect on most code pages because most input data is composed already. Consider calling [NormalizeString](../winnls/nf-winnls-normalizestring.md) after converting with **MultiByteToWideChar**. **NormalizeString** provides more accurate, standard, and consistent data, and can also be faster. Note that for the [NORM_FORM](../winnls/ne-winnls-norm_form.md) enumeration being passed to **NormalizeString**, NormalizationC corresponds to MB_PRECOMPOSED and NormalizationD corresponds to MB_COMPOSITE.

The *lpMultiByteStr* and *lpWideCharStr* pointers must not be the same. If they are the same, the function fails, and [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns the value ERROR_INVALID_PARAMETER.

**MultiByteToWideChar** does not null-terminate an output string if the input string length is explicitly specified without a terminating null character. To null-terminate an output string for this function, the application should pass in -1 or explicitly count the terminating null character for the input string.

The function fails if MB_ERR_INVALID_CHARS is set and an invalid character is encountered in the source string. An invalid character is one of the following:

- A character that is not the default character in the source string, but translates to the default character when MB_ERR_INVALID_CHARS is not set.
- For DBCS strings, a character that has a lead byte but no valid trail byte.

Starting with Windows Vista, this function fully conforms with the Unicode 4.1 specification for UTF-8 and UTF-16. The function used on earlier operating systems encodes or decodes lone [surrogate](/windows/win32/Intl/surrogates-and-supplementary-characters) halves or mismatched surrogate pairs. Code written in earlier versions of Windows that rely on this behavior to encode random non-text binary data might run into problems. However, code that uses this function on valid UTF-8 strings will behave the same way as on earlier Windows operating systems.

**Windows XP:** To prevent the security problem of the non-shortest-form versions of UTF-8 characters, **MultiByteToWideChar** deletes these characters.

**Starting with Windows 8:** **MultiByteToWideChar** is declared in `Stringapiset.h`. Before Windows 8, it was declared in `Winnls.h`.

## Code example

```cpp
catch (std::exception e)
{
    // Save in-memory logging buffer to a log file on error.

    ::std::wstring wideWhat;
    if (e.what() != nullptr)
    {
        int convertResult = MultiByteToWideChar(CP_UTF8, 0, e.what(), (int)strlen(e.what()), NULL, 0);
        if (convertResult <= 0)
        {
            wideWhat = L"Exception occurred: Failure to convert its message text using MultiByteToWideChar: convertResult=";
            wideWhat += convertResult.ToString()->Data();
            wideWhat += L"  GetLastError()=";
            wideWhat += GetLastError().ToString()->Data();
        }
        else
        {
            wideWhat.resize(convertResult + 10);
            convertResult = MultiByteToWideChar(CP_UTF8, 0, e.what(), (int)strlen(e.what()), &wideWhat[0], (int)wideWhat.size());
            if (convertResult <= 0)
            {
                wideWhat = L"Exception occurred: Failure to convert its message text using MultiByteToWideChar: convertResult=";
                wideWhat += convertResult.ToString()->Data();
                wideWhat += L"  GetLastError()=";
                wideWhat += GetLastError().ToString()->Data();
            }
            else
            {
                wideWhat.insert(0, L"Exception occurred: ");
            }
        }
    }
    else
    {
        wideWhat = L"Exception occurred: Unknown.";
    }

    Platform::String^ errorMessage = ref new Platform::String(wideWhat.c_str());
    // The session added the channel at level Warning. Log the message at
    // level Error which is above (more critical than) Warning, which
    // means it will actually get logged.
    _channel->LogMessage(errorMessage, LoggingLevel::Error);
    SaveLogInMemoryToFileAsync().then([=](StorageFile^ logFile) {
        _logFileGeneratedCount++;
        StatusChanged(this, ref new LoggingScenarioEventArgs(LoggingScenarioEventType::LogFileGenerated, logFile->Path->Data()));
    }).wait();
}
```

Example from [Windows Universal Samples](https://github.com/microsoft/Windows-universal-samples/blob/master/Samples/Logging/cpp/LoggingSessionScenario.cpp) on GitHub.

## -see-also

[Unicode and Character Set Functions](/windows/win32/Intl/unicode-and-character-set-functions)

[Unicode and Character Sets](/windows/win32/Intl/unicode-and-character-sets)

[WideCharToMultiByte](nf-stringapiset-widechartomultibyte.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
