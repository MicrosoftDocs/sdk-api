---
UID: NF:muiload.LoadMUILibraryW
title: LoadMUILibraryW function
author: windows-sdk-content
description: Returns a handle to the language-specific resources associated with a particular language-neutral (LN) file.
old-location: intl\loadmuilibrary.htm
old-project: Intl
ms.assetid: 277067d8-c38d-4e79-9c1a-4e4af1987228
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: LoadMUILibrary, LoadMUILibrary function [Internationalization for Windows Applications], LoadMUILibraryA, LoadMUILibraryW, MUI_LANGUAGE_EXACT, MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, _win32_LoadMUILibrary, intl.loadmuilibrary, muiload/LoadMUILibrary, muiload/LoadMUILibraryA, muiload/LoadMUILibraryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: muiload.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMUILibraryW (Unicode) and LoadMUILibraryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MTP_COMMAND_DATA_OUT, *PMTP_COMMAND_DATA_OUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Muiload.lib
api_name:
 - LoadMUILibrary
 - LoadMUILibraryA
 - LoadMUILibraryW
product: Windows
targetos: Windows
req.lib: Muiload.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LoadMUILibraryW function


## -description


Returns a handle to the language-specific resources associated with a particular language-neutral (LN) file.
<div class="alert"><b>Note</b>  To ensure that the DLL is unloaded correctly, your applications should match each call to <b>LoadMUILibrary</b> with a corresponding call to <a href="https://msdn.microsoft.com/38a0d7cb-46a9-449b-8f7e-4c573e400e75">FreeMUILibrary</a>.</div><div> </div>

## -parameters




### -param pszFullModuleName [in]

Pointer to a null-terminated string specifying the name of an LN file.


### -param dwLangConvention [in]

Flags specifying the naming convention on pre-Windows Vista operating systems to name the directories containing the language-specific resource files. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_ID"></a><a id="mui_language_id"></a><dl>
<dt><b>MUI_LANGUAGE_ID</b></dt>
</dl>
</td>
<td width="60%">
Interpret the name of the folder containing the language-specific resource files using <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Interpret the name of the folder containing the language-specific resource files using <a href="https://msdn.microsoft.com/e8c54168-22b3-435e-b19a-9b34adcdb018">language name</a> format.

</td>
</tr>
</table>
 

The following flag is available as an option and can be used in combination with either of the other flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_EXACT"></a><a id="mui_language_exact"></a><dl>
<dt><b>MUI_LANGUAGE_EXACT</b></dt>
</dl>
</td>
<td width="60%">
If resources for the identified language are not found in the resource files, check the main module specified by <i>pwszModuleName</i> and return a handle to that module if successful. 
	

</td>
</tr>
</table>
 


### -param LangID [in]

Language identifier for the user interface resources on a pre-Windows Vista operating system. The language identifier cannot correspond to the language associated with any of these locale information constants: 


<ul>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

## -returns



Returns a handle to the appropriate language-specific resource file if successful.

This function returns <b>NULL</b> if it fails. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function allows applications developed using the Win32 MUI resource technology to determine correctly the language-specific resource file to load on pre-Windows Vista operating systems. Applications using this function do not specifically have to be built on Windows Vista, but they do have to link statically with the MUILoad library provided in the Microsoft Windows SDK for Windows Vista. This function requires the executable and language-specific resource files to be stored using standard conventions. See <a href="https://msdn.microsoft.com/6c10b355-9bdd-4dba-8446-91034d4fe9b8">Application Deployment</a> for further information about file placement.

The following items influence the loading of satellite binaries by this function.

<ul>
<li>Operating system version running the application that calls the function</li>
<li>Flag passed in the <i>dwLangConvention</i> parameter</li>
<li>State of the language identifier passed in the <i>LangID</i> parameter</li>
</ul>
When running on Windows Vista, this function loads the main module without redirection. Only the <i>pszFullModuleName</i> parameter is used, as the resource loader functions perform redirection appropriately when they are called. When running on pre-Windows Vista operating systems, this function takes into account all parameters that the application supplies. It redirects binary loading to the proper satellite binary pair associated with the file represented by <i>pszFullModuleName</i>. This process reconstitutes the path associated with the file to mimic the behavior of Windows Vista that underlies the resource loader functions.

The application uses the <i>dwLangConvention</i> parameter to specify the way the satellite binaries should be probed. If the application sets this parameter to MUI_LANGUAGE_ID, the binaries are probed in folders with hexadecimal string values. (These values do not include the leading 0x, and are 4 characters in length. For example, en-US is represented 

as "0409" and en as "0009".) If the application sets the parameter to MUI_LANGUAGE_NAME, the function uses Windows Vista resource loading, which uses language name-based folder probes to find a satellite file.

The state of the language identifier in the <i>LangID</i> parameter affects resource probing. If the application sets this parameter to 0, the function uses the predefined fallback logic, dependent on the operating system, to locate the appropriate language-specific resource file. When the application sets <i>LangID</i> to a nonzero value, the probing mechanism only searches the appropriately named folder and its associated neutral equivalent. For more information, see <a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>.

<b>LoadMUILibrary</b> is built on the function <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>, and similar considerations need to be applied to its usage. In particular, <a href="https://msdn.microsoft.com/38a0d7cb-46a9-449b-8f7e-4c573e400e75">FreeMUILibrary</a> should be called for any handle returned by <b>LoadMUILibrary</b>. Also, <b>LoadMUILibrary</b> should not be called from <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>. For more information see the Remarks sections of <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> and <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.




## -see-also




<a href="https://msdn.microsoft.com/38a0d7cb-46a9-449b-8f7e-4c573e400e75">FreeMUILibrary</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

