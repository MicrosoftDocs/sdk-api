---
UID: NF:winnls.GetUserPreferredUILanguages
title: GetUserPreferredUILanguages function (winnls.h)
description: Retrieves information about the user preferred UI languages. For more information, see User Interface Language Management.
helpviewer_keywords: ["GetUserPreferredUILanguages","GetUserPreferredUILanguages function [Internationalization for Windows Applications]","MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","_win32_GetUserPreferredUILanguages","intl.getuserpreferreduilanguages","winnls/GetUserPreferredUILanguages"]
old-location: intl\getuserpreferreduilanguages.htm
tech.root: Intl
ms.assetid: 0800642c-c133-4993-bd16-6bdbf7518f1c
ms.date: 12/05/2018
ms.keywords: GetUserPreferredUILanguages, GetUserPreferredUILanguages function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, _win32_GetUserPreferredUILanguages, intl.getuserpreferreduilanguages, winnls/GetUserPreferredUILanguages
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - GetUserPreferredUILanguages
 - winnls/GetUserPreferredUILanguages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUserPreferredUILanguages
---

# GetUserPreferredUILanguages function


## -description

Retrieves information about the display language setting. For more information, see [User Interface Language Management](/windows/desktop/Intl/user-interface-language-management).

## -parameters

### -param dwFlags [in]

Flags identifying language format and filtering. The following flags specify the language format to use for the display language list. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

| Value | Meaning |
| --- | --- |
| **MUI_LANGUAGE_ID** | Retrieve the language strings in [language identifier](/windows/desktop/Intl/language-identifiers) |
| **MUI_LANGUAGE_NAME** | Retrieve the language strings in [language name](/windows/desktop/Intl/language-names) format. |

### -param pulNumLanguages [out]

Pointer to the number of languages retrieved in *pwszLanguagesBuffer*.

### -param pwszLanguagesBuffer [out, optional]

Optional. Pointer to a buffer in which this function retrieves an ordered, null-delimited display language list, in the format specified by *dwflags*. This list ends with two null characters.

Alternatively if this parameter is set to **NULL** and *pcchLanguagesBuffer* is set to 0, the function retrieves the required size of the language buffer in *pcchLanguagesBuffer*. The required size includes the two null characters.

### -param pcchLanguagesBuffer [in, out]

Pointer to the size, in characters, for the language buffer indicated by *pwszLanguagesBuffer*. On successful return from the function, the parameter contains the size of the retrieved language buffer.

Alternatively if this parameter is set to 0 and *pwszLanguagesBuffer* is set to **NULL**, the function retrieves the required size of the language buffer in *pcchLanguagesBuffer*.

## -returns

Returns **TRUE** if successful or **FALSE** otherwise. To get extended error information, the application can call [GetLastError function](../errhandlingapi/nf-errhandlingapi-getlasterror.md), which can return one of the following error codes:

- ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.

If the function fails for any other reason, the values of *pulNumLanguages* and *pcchLanguagesBuffer* are undefined.

## -remarks

When MUI_LANGUAGE_ID is specified, the language strings retrieved will be hexadecimal language identifiers that do not include the leading 0x, and will be 4 characters in length. For example, en-US will be returned as "0409" and en as "0009".

The display language cannot include more than one Language Interface Pack (LIP) language that corresponds to a [supplemental locale](/windows/desktop/Intl/custom-locales). If the list includes more than one of these languages, and if the application specifies MUI_LANGUAGE_ID in the call to the function, the language buffer contains "1400" for that language. This string corresponds to the hexadecimal value of [LOCALE_CUSTOM_UI_DEFAULT](/windows/desktop/Intl/locale-custom-constants).

The language list retrieved by this function has the following characteristics:

- Each language represents a valid NLS locale.
- Each language is installed on the operating system.
- The list contains one entry for each language, with no duplicate entries.
- If the list is empty or does not meet these validation criteria, the system preferred UI languages list is used instead.

### C# Signature

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetUserPreferredUILanguages(
            System.UInt32 dwFlags,
            ref System.UInt32 pulNumLanguages,
            System.IntPtr pwszLanguagesBuffer,
            ref System.UInt32 pcchLanguagesBuffer
            );

```

## -see-also

[GetSystemPreferredUILanguages function](nf-winnls-getsystempreferreduilanguages.md), [GetThreadPreferredUILanguages function](nf-winnls-getthreadpreferreduilanguages.md), [GetThreadUILanguage function](nf-winnls-getthreaduilanguage.md), [SetThreadPreferredUILanguages function](nf-winnls-setthreadpreferreduilanguages.md), [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface), [Multilingual User Interface Functions](/windows/desktop/Intl/multilingual-user-interface-functions)

