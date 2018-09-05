---
UID: NF:msiquery.MsiGetSourcePathA
title: MsiGetSourcePathA function
author: windows-sdk-content
description: The MsiGetSourcePath function returns the full source path for a folder in the Directory table.
old-location: setup\msigetsourcepath.htm
old-project: msi
ms.assetid: 3cb8c3fa-6f0a-4829-befd-450e58c86962
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MsiGetSourcePath, MsiGetSourcePath function, MsiGetSourcePathA, MsiGetSourcePathW, _msi_msigetsourcepath, msiquery/MsiGetSourcePath, msiquery/MsiGetSourcePathA, msiquery/MsiGetSourcePathW, setup.msigetsourcepath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetSourcePathW (Unicode) and MsiGetSourcePathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetSourcePath
 - MsiGetSourcePathA
 - MsiGetSourcePathW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetSourcePathA function


## -description


The 
<b>MsiGetSourcePath</b> function returns the full source path for a folder in the 
<a href="https://msdn.microsoft.com/eaca30cb-fec1-49ca-8b23-5e54c583e3e2">Directory table</a>.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFolder [in]

A null-terminated string that specifies a record of the 
<a href="https://msdn.microsoft.com/eaca30cb-fec1-49ca-8b23-5e54c583e3e2">Directory table</a>. If the directory is a root directory, this can be a value from the DefaultDir column. Otherwise it must be a value from the Directory column.


### -param szPathBuf [out]

Pointer to the buffer that receives the null terminated full source path. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szPathBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns ERROR_MORE_DATA and <i>pcchPathBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of ERROR_SUCCESS, <i>pcchPathBuf</i> contains the number of TCHARs written to the buffer, not including the terminating null character.


### -param pcchPathBuf [in, out]

Pointer to the variable that specifies the size, in TCHARs, of the buffer pointed to by the variable <i>szPathBuf</i>. When the function returns ERROR_SUCCESS, this variable contains the size of the data copied to <i>szPathBuf</i>, not including the terminating null character. If <i>szPathBuf</i> is not large enough, the function returns ERROR_MORE_DATA and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchPathBuf</i>.


## -returns



The 
<b>MsiGetSourcePath</b> function returns the following values:




## -remarks



Before calling this function, the installer must first run the 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize action</a>, 
<a href="https://msdn.microsoft.com/1b3f2baf-6191-452e-955d-8ac903edc1b7">FileCost action</a>, and 
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize action</a>. For more information, see <a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions from Programs</a>.

If ERROR_MORE_DATA is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If ERROR_SUCCESS is returned, it gives the number of characters written to the string buffer. Therefore you can get the size of the buffer by passing in an empty string (for example "") for the parameter that specifies the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Installer Location Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

