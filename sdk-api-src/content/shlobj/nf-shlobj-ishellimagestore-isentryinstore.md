---
UID: NF:shlobj.IShellImageStore.IsEntryInStore
title: IShellImageStore::IsEntryInStore (shlobj.h)
description: Checks to see if the image is in the store.
helpviewer_keywords: ["IShellImageStore interface [Windows Shell]","IsEntryInStore method","IShellImageStore.IsEntryInStore","IShellImageStore::IsEntryInStore","IsEntryInStore","IsEntryInStore method [Windows Shell]","IsEntryInStore method [Windows Shell]","IShellImageStore interface","_win32_IShellImageStore_IsEntryInStore","shell.IShellImageStore_IsEntryInStore","shlobj/IShellImageStore::IsEntryInStore"]
old-location: shell\IShellImageStore_IsEntryInStore.htm
tech.root: shell
ms.assetid: 571df609-9d17-415c-a4e0-23c4e1523993
ms.date: 12/05/2018
ms.keywords: IShellImageStore interface [Windows Shell],IsEntryInStore method, IShellImageStore.IsEntryInStore, IShellImageStore::IsEntryInStore, IsEntryInStore, IsEntryInStore method [Windows Shell], IsEntryInStore method [Windows Shell],IShellImageStore interface, _win32_IShellImageStore_IsEntryInStore, shell.IShellImageStore_IsEntryInStore, shlobj/IShellImageStore::IsEntryInStore
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
 - IShellImageStore::IsEntryInStore
 - shlobj/IShellImageStore::IsEntryInStore
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
 - IShellImageStore.IsEntryInStore
---

# IShellImageStore::IsEntryInStore


## -description

Checks to see if the image is in the store.

## -parameters

### -param pszName [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that specifies the path to the file that contains the image.

### -param pftTimeStamp [out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>*</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the time stamp for the image.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The entry is in the store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The entry is not in the store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The store is not open.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>