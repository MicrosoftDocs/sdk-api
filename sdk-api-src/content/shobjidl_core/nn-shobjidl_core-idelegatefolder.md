---
UID: NN:shobjidl_core.IDelegateFolder
title: IDelegateFolder (shobjidl_core.h)
description: Exposes a method through which a delegate folder is given the IMalloc interface required to allocate and free item IDs.
helpviewer_keywords: ["IDelegateFolder","IDelegateFolder interface [Windows Shell]","IDelegateFolder interface [Windows Shell]","described","shell.IDelegateFolder","shell_IDelegateFolder","shobjidl_core/IDelegateFolder"]
old-location: shell\IDelegateFolder.htm
tech.root: shell
ms.assetid: 16db01f3-4167-43f0-9ef7-34eec906e199
ms.date: 12/05/2018
ms.keywords: IDelegateFolder, IDelegateFolder interface [Windows Shell], IDelegateFolder interface [Windows Shell],described, shell.IDelegateFolder, shell_IDelegateFolder, shobjidl_core/IDelegateFolder
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDelegateFolder
 - shobjidl_core/IDelegateFolder
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
 - IDelegateFolder
---

# IDelegateFolder interface


## -description

Exposes a method through which a delegate folder is given the <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface required to allocate and free item IDs.

## -inheritance

The <b>IDelegateFolder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDelegateFolder</b> also has these types of members:

## -remarks

The IDs allocated by the delegate folder are in the form of <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid">DELEGATEITEMID</a> structures. It is the delegate's job to pack its data into the pointer to an item identifier list (PIDL) in the <b>DELEGATEITEMID</b> format.
