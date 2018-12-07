---
UID: NF:shlobj.IShellImageStore.Open
title: IShellImageStore::Open
author: windows-sdk-content
description: Opens the store and returns a lock.
old-location: shell\IShellImageStore_Open.htm
tech.root: shell
ms.assetid: 2aebf791-7681-42b3-8ffe-46e103e7c036
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellImageStore interface [Windows Shell],Open method, IShellImageStore.Open, IShellImageStore::Open, Open, Open method [Windows Shell], Open method [Windows Shell],IShellImageStore interface, _win32_IShellImageStore_Open, shell.IShellImageStore_Open, shlobj/IShellImageStore::Open
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
 - IShellImageStore.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageStore::Open


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/746bd660-17b6-4669-8f23-254f5d7dde82">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.]

Opens the store and returns a lock.


## -parameters




### -param dwMode

Type: <b>DWORD</b>

The storage instantiation mode specified by one of the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> values.


### -param pdwLock [out]

Type: <b>DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that receives the lock.


## -returns



Type: <b>HRESULT</b>

If the process is successful, the method returns the result of <a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>. Otherwise, it returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The storage is already open with the instantiation mode specified by <i>dwMode</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred. For example, store path is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
You do not have access to open the storage with the permissions specified by <i>dwMode</i>.

</td>
</tr>
</table>
 



