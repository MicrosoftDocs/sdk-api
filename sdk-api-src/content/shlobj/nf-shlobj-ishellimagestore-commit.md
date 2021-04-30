---
UID: NF:shlobj.IShellImageStore.Commit
title: IShellImageStore::Commit (shlobj.h)
description: Writes the contents specified by pdwLoc to storage.
helpviewer_keywords: ["Commit","Commit method [Windows Shell]","Commit method [Windows Shell]","IShellImageStore interface","IShellImageStore interface [Windows Shell]","Commit method","IShellImageStore.Commit","IShellImageStore::Commit","_win32_IShellImageStore_Commit","shell.IShellImageStore_Commit","shlobj/IShellImageStore::Commit"]
old-location: shell\IShellImageStore_Commit.htm
tech.root: shell
ms.assetid: 99ae5347-b140-4698-9fc5-bd60870d9149
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Shell], Commit method [Windows Shell],IShellImageStore interface, IShellImageStore interface [Windows Shell],Commit method, IShellImageStore.Commit, IShellImageStore::Commit, _win32_IShellImageStore_Commit, shell.IShellImageStore_Commit, shlobj/IShellImageStore::Commit
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
 - IShellImageStore::Commit
 - shlobj/IShellImageStore::Commit
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
 - IShellImageStore.Commit
---

# IShellImageStore::Commit


## -description

Writes the contents specified by <i>pdwLoc</i> to storage.

## -parameters

### -param pdwLock [in]

Type: <b>const DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that specifies the address that receives the lock.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value, including the following:

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
Content was saved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Saving was unsuccessful. The storage is not open or is open without write access.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>