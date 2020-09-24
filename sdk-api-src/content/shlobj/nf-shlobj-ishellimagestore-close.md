---
UID: NF:shlobj.IShellImageStore.Close
title: IShellImageStore::Close (shlobj.h)
description: Closes the image cache.
helpviewer_keywords: ["Close","Close method [Windows Shell]","Close method [Windows Shell]","IShellImageStore interface","IShellImageStore interface [Windows Shell]","Close method","IShellImageStore.Close","IShellImageStore::Close","_win32_IShellImageStore_Close","shell.IShellImageStore_Close","shlobj/IShellImageStore::Close"]
old-location: shell\IShellImageStore_Close.htm
tech.root: shell
ms.assetid: 6228228a-1c12-467c-849c-b360d79ee5ca
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Shell], Close method [Windows Shell],IShellImageStore interface, IShellImageStore interface [Windows Shell],Close method, IShellImageStore.Close, IShellImageStore::Close, _win32_IShellImageStore_Close, shell.IShellImageStore_Close, shlobj/IShellImageStore::Close
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
 - IShellImageStore::Close
 - shlobj/IShellImageStore::Close
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
 - IShellImageStore.Close
---

# IShellImageStore::Close


## -description

Closes the image cache.

## -parameters

### -param pdwLock [in]

Type: <b>const DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that specifies the address that receives the lock during the call to the <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-open">IShellImageStore::Open</a> method.

## -returns

Type: <b>HRESULT</b>

Returns S_FALSE if the store is not open or if the store cannot be saved. Returns the result of <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-commit">IShellImageStore::Commit</a> otherwise.

## -remarks

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore">IShellImageStore</a> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>