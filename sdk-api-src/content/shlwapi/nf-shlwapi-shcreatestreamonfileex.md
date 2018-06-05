---
UID: NF:shlwapi.SHCreateStreamOnFileEx
title: SHCreateStreamOnFileEx function
author: windows-sdk-content
description: Opens or creates a file and retrieves a stream to read or write to that file.
old-location: shell\SHCreateStreamOnFileEx.htm
old-project: shell
ms.assetid: f948f7dd-987d-4c2d-b650-62081133c3f4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHCreateStreamOnFileEx, SHCreateStreamOnFileEx function [Windows Shell], _shell_SHCreateStreamOnFileEx, shell.SHCreateStreamOnFileEx, shlwapi/SHCreateStreamOnFileEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
-	ShCore.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
-	API-MS-Win-ShCore-stream-l1-1-0.dll
api_name:
-	SHCreateStreamOnFileEx
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHCreateStreamOnFileEx function


## -description


Opens or creates a file and retrieves a stream to read or write to that file.


## -parameters




### -param pszFile [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that specifies the file name.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> values that are used to specify the file access mode and how the object that exposes the stream is created and deleted.


### -param dwAttributes [in]

Type: <b>DWORD</b>

One or more flag values that specify file attributes in the case that a new file is created. For a complete list of possible values, see the <i>dwFlagsAndAttributes</i> parameter of the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.


### -param fCreate [in]

Type: <b>BOOL</b>

A <b>BOOL</b> value that helps specify, in conjunction with <i>grfMode</i>, how existing files should be treated when creating the stream. See Remarks for details.


### -param pstmTemplate [in, optional]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Reserved.


### -param ppstm [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

Receives an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointer for the stream associated with the file.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>SHCreateStreamOnFileEx</b> function extends the semantics of the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> flags and produces the same effect as calling the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.

The <i>grfMode</i> and <i>fCreate</i> parameters work together to specify how the function should behave with respect to existing files.



<table class="clsStd">
<tr>
<th><i>grfMode</i></th>
<th><i>fCreate</i></th>
<th>File exists?</th>
<th>Behavior</th>
</tr>
<tr>
<td><b>STGM_CREATE</b></td>
<td>Ignored</td>
<td>Yes</td>
<td>The file is recreated.</td>
</tr>
<tr>
<td><b>STGM_CREATE</b></td>
<td>Ignored</td>
<td>No</td>
<td>The file is created.</td>
</tr>
<tr>
<td><b>STGM_FAILIFTHERE</b></td>
<td><b>FALSE</b></td>
<td>Yes</td>
<td>The file is opened.</td>
</tr>
<tr>
<td><b>STGM_FAILIFTHERE</b></td>
<td><b>FALSE</b></td>
<td>No</td>
<td>The call fails.</td>
</tr>
<tr>
<td><b>STGM_FAILIFTHERE</b></td>
<td><b>TRUE</b></td>
<td>Yes</td>
<td>The call fails.</td>
</tr>
<tr>
<td><b>STGM_FAILIFTHERE</b></td>
<td><b>TRUE</b></td>
<td>No</td>
<td>The file is created.</td>
</tr>
</table>
 



