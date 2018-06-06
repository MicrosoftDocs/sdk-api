---
UID: NF:winver.VerLanguageNameW
title: VerLanguageNameW function
author: windows-sdk-content
description: Retrieves a description string for the language associated with a specified binary Microsoft language identifier.
old-location: menurc\verlanguagename.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\verlanguagename.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: VerLanguageName, VerLanguageName function [Menus and Other Resources], VerLanguageNameA, VerLanguageNameW, _win32_VerLanguageName, _win32_verlanguagename_cpp, menurc.verlanguagename, winui._win32_verlanguagename, winver/VerLanguageName, winver/VerLanguageNameA, winver/VerLanguageNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Mincore.lib
req.dll: Api-ms-win-core-localization-l1-2-1.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# VerLanguageNameW function


## -description


Retrieves a description string for the language associated with a specified binary Microsoft language identifier.


## -parameters




### -param wLang [in]

Type: <b>DWORD</b>

The binary language identifier. For a complete list of the language identifiers, see <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>.

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

Typically, an installation program uses this function to translate a language identifier returned by the <a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a> function. The text string may be used in a dialog box that asks the user how to proceed in the event of a language conflict. 




## -see-also




<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information Overview</a>
 

 

