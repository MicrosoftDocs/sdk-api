---
UID: NF:shlobj.IShellImageStore.Open
title: IShellImageStore::Open (shlobj.h)
description: Opens the store and returns a lock.
helpviewer_keywords: ["IShellImageStore interface [Windows Shell]","Open method","IShellImageStore.Open","IShellImageStore::Open","Open","Open method [Windows Shell]","Open method [Windows Shell]","IShellImageStore interface","_win32_IShellImageStore_Open","shell.IShellImageStore_Open","shlobj/IShellImageStore::Open"]
old-location: shell\IShellImageStore_Open.htm
tech.root: shell
ms.assetid: 2aebf791-7681-42b3-8ffe-46e103e7c036
ms.date: 12/05/2018
ms.keywords: IShellImageStore interface [Windows Shell],Open method, IShellImageStore.Open, IShellImageStore::Open, Open, Open method [Windows Shell], Open method [Windows Shell],IShellImageStore interface, _win32_IShellImageStore_Open, shell.IShellImageStore_Open, shlobj/IShellImageStore::Open
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageStore::Open
 - shlobj/IShellImageStore::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageStore.Open
---

# IShellImageStore::Open


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.]

Opens the store and returns a lock.

## -parameters

### -param dwMode

Type: <b>DWORD</b>

The storage instantiation mode specified by one of the <a href="/windows/desktop/Stg/stgm-constants">STGM</a> values.

### -param pdwLock [out]

Type: <b>DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that receives the lock.

## -returns

Type: <b>HRESULT</b>

If the process is successful, the method returns the result of <a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage">StgOpenStorage</a>. Otherwise, it returns one of the following values:

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