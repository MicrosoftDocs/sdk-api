---
UID: NF:shobjidl_core.IDelegateFolder.SetItemAlloc
title: IDelegateFolder::SetItemAlloc (shobjidl_core.h)
author: windows-sdk-content
description: Provides the delegate folder an IMalloc interface used to allocate and free item IDs.
old-location: shell\IDelegateFolder_SetItemAlloc.htm
tech.root: shell
ms.assetid: ce1ee472-e245-4112-858a-1d9739f5a36d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDelegateFolder interface [Windows Shell],SetItemAlloc method, IDelegateFolder.SetItemAlloc, IDelegateFolder::SetItemAlloc, SetItemAlloc, SetItemAlloc method [Windows Shell], SetItemAlloc method [Windows Shell],IDelegateFolder interface, shell.IDelegateFolder_SetItemAlloc, shell_IDelegateFolder_SetItemAlloc, shobjidl_core/IDelegateFolder::SetItemAlloc
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDelegateFolder.SetItemAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDelegateFolder::SetItemAlloc


## -description


Provides the delegate folder an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface used to allocate and free item IDs.


## -parameters




### -param pmalloc [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



