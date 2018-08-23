---
UID: NF:winnls.EnumSystemLanguageGroupsA
title: EnumSystemLanguageGroupsA function
author: windows-sdk-content
description: Enumerates the language groups that are either installed on or supported by an operating system.
old-location: intl\enumsystemlanguagegroups.htm
old-project: Intl
ms.assetid: 8cc2335e-b222-44d9-a966-4b6803639071
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: EnumSystemLanguageGroups, EnumSystemLanguageGroups function [Internationalization for Windows Applications], EnumSystemLanguageGroupsA, EnumSystemLanguageGroupsW, LGRPID_INSTALLED, LGRPID_SUPPORTED, _win32_EnumSystemLanguageGroups, intl.enumsystemlanguagegroups, winnls/EnumSystemLanguageGroups, winnls/EnumSystemLanguageGroupsA, winnls/EnumSystemLanguageGroupsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumSystemLanguageGroupsW (Unicode) and EnumSystemLanguageGroupsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumSystemLanguageGroups
 - EnumSystemLanguageGroupsA
 - EnumSystemLanguageGroupsW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumSystemLanguageGroupsA function


## -description


Enumerates the language groups that are either installed on or supported by an operating system. <div class="alert"><b>Note</b>  For custom locales, your application should call <a href="https://msdn.microsoft.com/74b1b453-66e9-4724-a956-26cea2d7d744">EnumSystemLocalesEx</a> instead of <b>EnumSystemLanguageGroups</b>.</div>
<div> </div>



## -parameters




### -param lpLanguageGroupEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/ea771874-61c7-4f5b-a4ca-9ed3c5698b2d">EnumLanguageGroupsProc</a>.


### -param dwFlags [in]

Flags specifying the language group identifiers to enumerate. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LGRPID_INSTALLED"></a><a id="lgrpid_installed"></a><dl>
<dt><b>LGRPID_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only installed language group identifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="LGRPID_SUPPORTED"></a><a id="lgrpid_supported"></a><dl>
<dt><b>LGRPID_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all supported language group identifiers.

</td>
</tr>
</table>
 


### -param lParam [in]

Application-defined value to pass to the callback function. This parameter can be used in error checking. It can also be used to ensure thread safety in the callback function.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates language groups by passing language group identifiers, one at a time, to the specified application-defined callback function. This process continues until the last language group identifier is found or the callback function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/5a85c6bd-0362-46ff-80be-a198b1259482">EnumLanguageGroupLocales</a>



<a href="https://msdn.microsoft.com/ea771874-61c7-4f5b-a4ca-9ed3c5698b2d">EnumLanguageGroupsProc</a>



<a href="https://msdn.microsoft.com/68cf09f8-fe97-4035-94b6-886ca26bbf3e">IsValidLanguageGroup</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

