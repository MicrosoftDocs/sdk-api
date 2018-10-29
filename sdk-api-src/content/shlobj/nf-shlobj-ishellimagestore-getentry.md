---
UID: NF:shlobj.IShellImageStore.GetEntry
title: IShellImageStore::GetEntry
author: windows-sdk-content
description: Gets a handle to an image in the cache.
old-location: shell\IShellImageStore_GetEntry.htm
tech.root: shell
ms.assetid: 580e2901-ae08-4c9f-99ee-7ba2f7fe6e52
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetEntry, GetEntry method [Windows Shell], GetEntry method [Windows Shell],IShellImageStore interface, IShellImageStore interface [Windows Shell],GetEntry method, IShellImageStore.GetEntry, IShellImageStore::GetEntry, _win32_IShellImageStore_GetEntry, shell.IShellImageStore_GetEntry, shlobj/IShellImageStore::GetEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageStore.GetEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageStore::GetEntry


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/746bd660-17b6-4669-8f23-254f5d7dde82">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.]

Gets a handle to an image in the cache.


## -parameters




### -param pszName [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that specifies the path to the file that contains the image.


### -param dwMode

Type: <b>DWORD</b>

The storage instantiation mode specified by one of the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM </a>values.


### -param phImage [out]

Type: <b>HBITMAP*</b>

A pointer to the handle of the bitmap.


## -returns



Type: <b>HRESULT</b>

Returns the result of <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> if the process was successful. Otherwise, returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Storage is not open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The stream cannot be found.

</td>
</tr>
</table>
 




## -remarks



It is the caller's responsibility to free the handle after a call to this method.



