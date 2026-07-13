---
UID: NF:winnls.GetFileMUIPath
title: GetFileMUIPath function (winnls.h)
description: Retrieves the path to all language-specific resource files associated with the supplied LN file. The application must call this function repeatedly to get the path for each resource file.
helpviewer_keywords: ["GetFileMUIPath","GetFileMUIPath function [Internationalization for Windows Applications]","MUI_LANGUAGE_ID","MUI_LANGUAGE_NAME","MUI_LANG_NEUTRAL_PE_FILE","MUI_NON_LANG_NEUTRAL_FILE","MUI_USER_PREFERRED_UI_LANGUAGES","MUI_USE_INSTALLED_LANGUAGES","MUI_USE_SEARCH_ALL_LANGUAGES","_win32_GetFileMUIPath","intl.getfilemuipath","winnls/GetFileMUIPath"]
old-location: intl\getfilemuipath.htm
tech.root: Intl
ms.assetid: a95ef85a-4a3a-49c6-b700-03763950c64f
ms.date: 12/05/2018
ms.keywords: GetFileMUIPath, GetFileMUIPath function [Internationalization for Windows Applications], MUI_LANGUAGE_ID, MUI_LANGUAGE_NAME, MUI_LANG_NEUTRAL_PE_FILE, MUI_NON_LANG_NEUTRAL_FILE, MUI_USER_PREFERRED_UI_LANGUAGES, MUI_USE_INSTALLED_LANGUAGES, MUI_USE_SEARCH_ALL_LANGUAGES, _win32_GetFileMUIPath, intl.getfilemuipath, winnls/GetFileMUIPath
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
 - GetFileMUIPath
 - winnls/GetFileMUIPath
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
 - GetFileMUIPath
---

# GetFileMUIPath function


## -description

Retrieves the path to all language-specific resource files associated with the supplied LN file. The application must call this function repeatedly to get the path for each resource file.

## -parameters

### -param dwFlags [in]

Flags identifying language format and filtering. The following flags specify the format of the language indicated by <i>pwszLanguage</i>. The flags are mutually exclusive, and the default is MUI_LANGUAGE_NAME.

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
Retrieve the language string in <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> format.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_LANGUAGE_NAME"></a><a id="mui_language_name"></a><dl>
<dt><b>MUI_LANGUAGE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the language string in <a href="/windows/desktop/Intl/language-names">language name</a> format.

</td>
</tr>
</table>
 

The following flags specify the filtering for the function to use in locating language-specific resource files if <i>pwszLanguage</i> is set to <b>NULL</b>. The filtering flags are mutually exclusive, and the default is MUI_USER_PREFERRED_UI_LANGUAGES.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_USE_SEARCH_ALL_LANGUAGES"></a><a id="mui_use_search_all_languages"></a><dl>
<dt><b>MUI_USE_SEARCH_ALL_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Retrieve all language-specific resource files for the path indicated by <i>pcwszFilePath</i>, without considering file licensing. This flag is relevant only if the application supplies a null string for <i>pwszLanguage</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_USER_PREFERRED_UI_LANGUAGES"></a><a id="mui_user_preferred_ui_languages"></a><dl>
<dt><b>MUI_USER_PREFERRED_UI_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Retrieve only the files that implement languages in the fallback list. Successive calls enumerate the successive fallbacks, in the appropriate order. The first file indicated by the output value of <i>pcchFileMUIPath</i> should be the best fit. This flag is relevant only if the application supplies a null string for <i>pwszLanguage</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_USE_INSTALLED_LANGUAGES"></a><a id="mui_use_installed_languages"></a><dl>
<dt><b>MUI_USE_INSTALLED_LANGUAGES</b></dt>
</dl>
</td>
<td width="60%">
Retrieve only the files for the languages installed on the computer. This flag is relevant only if the application supplies a null string for <i>pwszLanguage</i>.

</td>
</tr>
</table>
 

The following flags allow the user to indicate the type of file that is specified by <i>pcwszFilePath</i> so that the function can determine if it must add ".mui" to the file name. The flags are mutually exclusive. If the application passes both flags, the function fails. If the application passes neither flag, the function checks the file in the root folder to verify the file type and decide on file naming.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MUI_LANG_NEUTRAL_PE_FILE"></a><a id="mui_lang_neutral_pe_file"></a><dl>
<dt><b>MUI_LANG_NEUTRAL_PE_FILE</b></dt>
</dl>
</td>
<td width="60%">
Do not verify the file passed in <i>pcwszFilePath</i> and append ".mui" to the file name before processing. For example, change Abc.exe to Abc.exe.mui.

</td>
</tr>
<tr>
<td width="40%"><a id="MUI_NON_LANG_NEUTRAL_FILE"></a><a id="mui_non_lang_neutral_file"></a><dl>
<dt><b>MUI_NON_LANG_NEUTRAL_FILE</b></dt>
</dl>
</td>
<td width="60%">
Do not verify the file passed in <i>pcwszFilePath</i> and do not append ".mui" to the file name before processing. For example, use Abc.txt or Abc.chm.

</td>
</tr>
</table>

### -param pcwszFilePath [in]

Pointer to a null-terminated string specifying a file path. The path is either for an existing LN file or for a file such as a .txt, .inf, or .msc file. If the file is an LN file, the function looks for files containing the associated language-specific resources. For all other types of files, the function seeks files that correspond exactly to the file name and path indicated. Your application can overwrite the behavior of the file type check by using the MUI_LANG_NEUTRAL_PE_FILE or MUI_NON_LANG_NEUTRAL_FILE flag. For more information, see the Remarks section.

<div class="alert"><b>Note</b>  The supplied file path can be a network path: for example, "\\machinename\c$\windows\system32\notepad.exe".</div>
<div> </div>

### -param pwszLanguage [in, out, optional]

Pointer to a buffer containing a language string. On input, this buffer contains the language identifier or language name for which the application should find language-specific resource files, depending on the settings of <i>dwFlags</i>. On successful return from the function, this parameter contains the language of the language-specific resource file that the function has found.

Alternatively, the application can set this parameter to <b>NULL</b>, with the value referenced by  <i>pcchLanguage</i> set to 0. In this case, the function retrieves the required buffer size in <i>pcchLanguage</i>.

### -param pcchLanguage [in, out]

Pointer to the buffer size, in characters, for the language string indicated by <i>pwszLanguage</i>. If the application sets the value referenced by this parameter to 0 and  passes <b>NULL</b> for <i>pwszLanguage</i>, then the required buffer size will be returned in <i>pcchLanguage</i> and the returned buffer size is always <a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_MAX_LENGTH</a>, because the function is typically called multiple times in succession. The function cannot determine the exact size of the language name for all successive calls, and cannot extend the buffer on subsequent calls. Thus LOCALE_NAME_MAX_LENGTH is the only safe maximum.

### -param pwszFileMUIPath [out, optional]

Pointer to a buffer containing the path to the language-specific resource file. It is strongly recommended to allocate this buffer to be of size MAX_PATH.

Alternatively, this parameter can retrieve <b>NULL</b> if the value referenced by <i>pcchFileMUIPath</i> is set to 0. In this case, the function retrieves the required size for the file path buffer in <i>pcchFileMUIPath</i>.

### -param pcchFileMUIPath [in, out]

Pointer to the buffer size, in characters, for the file path indicated by <i>pwszFileMUIPath</i>. On successful return from the function, this parameter indicates the size of the retrieved file path. If the application sets the value referenced by this parameter to 0, the function retrieves <b>NULL</b> for <i>pwszFileMUIPath</i>, the required buffer size will be returned in <i>pcchFileMUIPath</i> and the returned buffer size is always MAX_PATH, because the function is typically called multiple times in succession. The function cannot determine the exact size of the path for all successive calls, and cannot extend the buffer on subsequent calls. Thus MAX_PATH is the only safe maximum.

### -param pululEnumerator [in, out]

Pointer to an enumeration variable. The first time this function is called, the value of the variable should be 0. Between subsequent calls, the application should not change the value of this parameter. After the function retrieves all possible language-specific resource file paths, it returns <b>FALSE</b>.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. If the function fails, the output parameters do not change.

To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_NO_MORE_FILES. There were no more files to process.</li>
</ul>

## -remarks

This function verifies that language-specific resource files exist, but it does not verify that they are correct. It requires the resource files to be stored according to the storage convention explained in <a href="/windows/desktop/Intl/application-deployment">Application Deployment</a>.

If the call to this function specifies the MUI_LANGUAGE_ID flag, the supplied language string must 

use a hexadecimal language identifier that does not include the leading 0x, and is 4 characters in length. 

For example, en-US should be passed as "0409" and en as "0009". The returned language string will be in the 

same format.

When MUI_LANGUAGE_ID is specified, each hexadecimal value in the supplied language string must represent an actual language identifier. In particular, the values corresponding to the following locales cannot be specified: 


<ul>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>
To receive enumerated information, the application should call this function repeatedly until it returns <b>FALSE</b>, leaving the contents of <i>pululEnumerator</i> unchanged between calls. Since each call retrieves the path to a different language-specific resource file, the application must clear the language buffer to an empty string between calls. If the application does not do this, the input value of <i>pwszLanguage</i> takes precedence over the setting of <i>dwFlags</i>.

Typically the resource loader is used to find resource files. However, your application can also use this function to find the files. If the input file path is for an LN file, the function attaches a suffix of ".mui" when looking for the corresponding language-specific resource files.

For example, the function retrieves the following files when the application passes the string "C:\mydir\Example1.dll" in <i>pcwszFilePath</i> as the root file path, with <i>dwFlags</i> set to MUI_LANGUAGE_NAME | MUI_USE_SEARCH_ALL_LANGUAGES:

<ul>
<li>C:\mydir\Example1.dll<ul>
<li>C:\mydir\en-US\Example1.dll.mui</li>
<li>C:\mydir\ja-JP\Example1.dll.mui</li>
</ul>
</li>
</ul>
The first call to the function sets <i>pwszFileMUIPath</i>  to "C:\mydir\en-US\Example1.dll.mui". The second call sets the file path to "C:\mydir\ja-JP\Example1.dll.mui". The function returns <b>FALSE</b> when called a third time and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_MORE_FILES.

If the file indicated by <i>pcwszFilePath</i> does not have resource configuration data, or if the file does not exist, the function leaves the file name as it is when looking for the corresponding language-specific resource files.

For example, the application passes the string "C:\mydir\Example2.txt" in <i>pcwszFilePath</i> as the root file path, with <i>dwFlags</i> set to MUI_LANGUAGE_NAME | MUI_USER_PREFERRED_UI_LANGUAGES. Let's consider the case in which the user preferred UI languages (in order) are Catalan, "ca-ES", and Spanish (Spain), "es-ES", and where the following files exist:

<ul>
<li>(no corresponding file in C:\mydir)
            <ul>
<li>C:\mydir\en-US\Example2.txt</li>
<li>C:\mydir\en\Example2.txt</li>
<li>C:\mydir\es-ES\Example2.txt</li>
<li>C:\mydir\es\Example2.txt</li>
<li>C:\mydir\ja-JP\Example2.txt</li>
</ul>
</li>
</ul>
The first call to the function determines that there are no resources for "ca-ES" or for the neutral language "ca". The function then tries the next option, "es-ES", for which it succeeds in finding a match. Before returning, the function sets <i>pwszFileMUIPath</i>  to "C:\mydir\es-ES\Example2.txt". A second application call to the function continues the enumeration by setting <i>pwszFileMUIPath</i> to "C:\mydir\es\Example2.txt".

If the target file and its associated resource files are actually <a href="/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal">Side-by-side enabled assemblies</a>, GetFileMUIPath cannot be used to retrieve the path to the resource file. Please refer to <a href="/windows/desktop/SbsCs/using-assemblies-with-a-multilanguage-user-interface">Using Assemblies with a Multilanguage User Interface</a> for details on how to use Side-by-side assemblies with MUI support.

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
[DllImport("Kernel32.dll", CharSet = CharSet.Auto)]
        static extern System.Boolean GetFileMUIPath(
            System.UInt32 dwFlags,
            System.String pcwszFilePath,
            System.Text.StringBuilder pwszLanguage,
            ref System.UInt32 pcchLanguage,
            System.Text.StringBuilder pwszFileMUIPath,
            ref System.UInt32 pcchFileMUIPath,
            ref System.UInt64 pululEnumerator
            );

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getthreaduilanguage">GetThreadUILanguage</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadpreferreduilanguages">SetThreadPreferredUILanguages</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreaduilanguage">SetThreadUILanguage</a>