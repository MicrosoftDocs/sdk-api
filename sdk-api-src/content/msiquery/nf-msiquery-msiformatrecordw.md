---
UID: NF:msiquery.MsiFormatRecordW
title: MsiFormatRecordW function
author: windows-sdk-content
description: The MsiFormatRecord function formats record field data and properties using a format string.
old-location: setup\msiformatrecord.htm
old-project: Msi
ms.assetid: 574f51b1-a5cf-46c8-bfa3-449839872cf3
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: MsiFormatRecord, MsiFormatRecord function, MsiFormatRecordA, MsiFormatRecordW, _msi_msiformatrecord, msiquery/MsiFormatRecord, msiquery/MsiFormatRecordA, msiquery/MsiFormatRecordW, setup.msiformatrecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiFormatRecordW (Unicode) and MsiFormatRecordA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
-	Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
-	MsiFormatRecord
-	MsiFormatRecordA
-	MsiFormatRecordW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiFormatRecordW function


## -description


The 
<b>MsiFormatRecord</b> function formats record field data and properties using a format string.


## -parameters




### -param hInstall [in]

Handle to the installation. This may be omitted, in which case only the record field parameters are processed and properties are not available for substitution.


### -param hRecord [in]

Handle to the record to format. The template string must be stored in record field 0 followed by referenced data parameters.


### -param szResultBuf [out]

Pointer to the buffer that receives the null terminated formatted string. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szResultBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns <b>ERROR_MORE_DATA</b> and <i>pcchResultBuf</i> contains the required buffer size in <b>TCHAR</b>s, not including the terminating null character. On return of <b>ERROR_SUCCESS</b>, <i>pcchResultBuf</i> contains the number of <b>TCHAR</b>s written to the buffer, not including the terminating null character.


### -param pcchResultBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHAR</b>s, of the buffer pointed to by the variable <i>szResultBuf</i>. When the function returns <b>ERROR_SUCCESS</b>, this variable contains the size of the data copied to <i>szResultBuf</i>, not including the terminating null character. If <i>szResultBuf</i> is not large enough, the function returns <b>ERROR_MORE_DATA</b> and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchResultBuf</i>.


## -returns



The 
<b>MsiFormatRecord</b> function returns one of the following values:




## -remarks



The 
<b>MsiFormatRecord</b> function uses the following format process.

Parameters that are to be 
<a href="https://msdn.microsoft.com/7a1bc160-a06c-4d57-b429-e39167893a45">formatted</a> are enclosed in square brackets [...]. The square brackets can be iterated because the substitutions are resolved from the inside out.

If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.

If a part of the string is enclosed in curly braces { } and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces. If any of the properties is not found, all the text in the braces and the braces themselves are removed.

Note in the case of deferred execution custom actions, 
<b>MsiFormatRecord</b> only supports <b>CustomActionData</b> and <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> properties. For more information, see 
<a href="https://msdn.microsoft.com/13174c5d-c810-4b5d-9d1e-60ed30b8c44d">Obtaining Context Information for Deferred Execution Custom Actions</a>.

The following steps describe how to format strings using the 
<b>MsiFormatRecord</b> function:

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To format strings using the MsiFormatRecord function</b>

<ol>
<li>The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or null values producing no text.</li>
<li>
The resultant string is processed by replacing the nonrecord parameters with the corresponding values, described next.

<ul>
<li>If a substring of the form "[propertyname]" is encountered, it is replaced by the value of the property.</li>
<li>If a substring of the form "[%environmentvariable]" is found, the value of the environment variable is substituted.</li>
<li>If a substring of the form" [#<i>filekey</i>]" is found, it is replaced by the full path of the file, with the value <i>filekey</i> used as a key into the 
<a href="https://msdn.microsoft.com/31d0e727-a9eb-4cd2-a211-ea7b138d0173">File table</a>. The value of "[#<i>filekey</i>]" remains blank and is not replaced by a path until the installer runs the 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize action</a>, 
<a href="https://msdn.microsoft.com/1b3f2baf-6191-452e-955d-8ac903edc1b7">FileCost action</a>, and 
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize action</a>. The value of "[#<i>filekey</i>]" depends upon the installation state of the component to which the file belongs. If the component is being run from source, the value is the path to the source location of the file. If the component is being run locally, the value is the path to the target location of the file after installation. If the component is absent, the path is blank. For more information about checking the installation state of components, see 
<a href="https://msdn.microsoft.com/c4547e5d-ea71-494f-9d92-c7fef23bcc0f">Checking the Installation of Features, Components, Files</a>.</li>
<li>If a substring of the form "[$<i>componentkey</i>]" is found, it is replaced by the install directory of the component, with the value <i>componentkey</i> used as a key into the 
<a href="https://msdn.microsoft.com/069d64e9-106a-42b7-8dea-a44fc0c6e0cd">Component table</a>. The value of "[$<i>componentkey</i>]" remains blank and is not replaced by a directory until the installer runs the 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize action</a>, 
<a href="https://msdn.microsoft.com/1b3f2baf-6191-452e-955d-8ac903edc1b7">FileCost action</a>, and 
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize action</a>. The value of "[$<i>componentkey</i>]" depends upon the installation state of the component. If the component is being run from source, the value is the source directory of the file. If the component is being run locally, the value is the target directory after installation. If the component is absent, the value is left blank. For more information about checking the installation state of components, see 
<a href="https://msdn.microsoft.com/c4547e5d-ea71-494f-9d92-c7fef23bcc0f">Checking the Installation of Features, Components, Files</a>.</li>
<li>Note that if a component is already installed, and is not being reinstalled, removed, or moved during the current installation, the action state of the component is null and therefore the string "[$componentkey]" evaluates to Null.</li>
<li>If a substring of the form "[\c]" is found, it is replaced by the character without any further processing. Only the first character after the backslash is kept; everything else is removed.</li>
</ul>
</li>
</ol>
If <b>ERROR_MORE_DATA</b> is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If <b>ERROR_SUCCESS</b> is returned, it gives the number of characters written to the string buffer. Therefore you can get the size of the buffer by passing in an empty string (for example "") for the parameter that specifies the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).




## -see-also




<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

