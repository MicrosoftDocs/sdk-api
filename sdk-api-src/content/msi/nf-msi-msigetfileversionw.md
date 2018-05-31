---
UID: NF:msi.MsiGetFileVersionW
title: MsiGetFileVersionW function
author: windows-sdk-content
description: The MsiGetFileVersion returns the version string and language string in the format that the installer expects to find them in the database.
old-location: setup\msigetfileversion.htm
old-project: Msi
ms.assetid: 9dd7d71e-2e76-4755-a979-f3dcdcd6ebec
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiGetFileVersion, MsiGetFileVersion function, MsiGetFileVersionA, MsiGetFileVersionW, _msi_msigetfileversion, msi/MsiGetFileVersion, msi/MsiGetFileVersionA, msi/MsiGetFileVersionW, setup.msigetfileversion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFileVersionW (Unicode) and MsiGetFileVersionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiGetFileVersion
-	MsiGetFileVersionA
-	MsiGetFileVersionW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetFileVersionW function


## -description


The 
<b>MsiGetFileVersion</b> returns the version string and language string in the format that the installer expects to find them in the database. If you want only version information, set <i>lpLangBuf</i> and <i>pcchLangBuf</i> to 0 (zero). If you just want language information, set <i>lpVersionBuf</i> and <i>pcchVersionBuf</i> to 0 (zero).


## -parameters




### -param szFilePath [in]

Specifies the path to the file.


### -param lpVersionBuf [out]

Returns the file version. 

Set to 0 for language information only.


### -param pcchVersionBuf [in, out]

In and out buffer count as the number of <b>TCHAR</b>. 

Set to 0 (zero) for language information only. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


### -param lpLangBuf [out]

Returns the file language. 

Set to 0 (zero) for version information only.


### -param pcchLangBuf [in, out]

In and out buffer count as the number of <b>TCHAR</b>. 

Set to 0 (zero) for version information only. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
Successful completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
File does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
File cannot be opened to get version information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
File does not contain version information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The version information is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

