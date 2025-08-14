---
UID: NF:winver.VerLanguageNameA
title: VerLanguageNameA function (winver.h)
description: Retrieves a description string for the language associated with a specified binary Microsoft language identifier. (ANSI)
helpviewer_keywords: ["VerLanguageNameA", "winver/VerLanguageNameA"]
old-location: menurc\verlanguagename.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\verlanguagename.htm
ms.date: 12/05/2018
ms.keywords: VerLanguageName, VerLanguageName function [Menus and Other Resources], VerLanguageNameA, VerLanguageNameW, _win32_VerLanguageName, _win32_verlanguagename_cpp, menurc.verlanguagename, winui._win32_verlanguagename, winver/VerLanguageName, winver/VerLanguageNameA, winver/VerLanguageNameW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VerLanguageNameW (Unicode) and VerLanguageNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Version.lib
req.dll: Api-ms-win-core-localization-l1-2-1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerLanguageNameA
 - winver/VerLanguageNameA
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
 - api-ms-win-core-localization-l1-2-1.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - kernel32.dll
api_name:
 - VerLanguageName
 - VerLanguageNameA
 - VerLanguageNameW
---

# VerLanguageNameA function


## -description

Retrieves a description string for the language associated with a specified binary Microsoft language identifier.

## -parameters

### -param wLang [in]

Type: <b>DWORD</b>

The binary language identifier. For a complete list of the language identifiers, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.

For example, the description string associated with the language identifier 0x040A is "Spanish (Traditional Sort)". If the identifier is unknown, the <i>szLang</i> parameter points to a default string ("Language Neutral").

### -param szLang [out]

Type: <b>LPTSTR</b>

The language specified by the <i>wLang</i> parameter.

### -param cchLang [in]

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <i>szLang</i>.

## -returns

Type: <b>DWORD</b>

The return value is the size, in characters, of the string returned in the buffer. This value does not include the terminating null character. If the description string is smaller than or equal to the buffer, the entire description string is in the buffer. If the description string is larger than the buffer, the description string is truncated to the length of the buffer.

If an error occurs, the return value is zero. Unknown language identifiers do not produce errors.

## -remarks

 This function works on 16-, 32-, and 64-bit file images.

Typically, an installation program uses this function to translate a language identifier returned by the <a href="/windows/desktop/api/winver/nf-winver-verqueryvaluea">VerQueryValue</a> function. The text string may be used in a dialog box that asks the user how to proceed in the event of a language conflict. 





> [!NOTE]
> The winver.h header defines VerLanguageName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/menurc/version-information">Version Information Overview</a>
