---
UID: NN:shobjidl_core.IDelegateItem
title: IDelegateItem (shobjidl_core.h)
description: Used to obtain the immediately underlying representation of an item's path.
helpviewer_keywords: ["IDelegateItem","IDelegateItem interface [Windows Shell]","IDelegateItem interface [Windows Shell]","described","_shell_IDelegateItem","shell.IDelegateItem","shobjidl_core/IDelegateItem"]
old-location: shell\IDelegateItem.htm
tech.root: shell
ms.assetid: aca76587-5f1d-4154-a68b-df162c38624e
ms.date: 12/05/2018
ms.keywords: IDelegateItem, IDelegateItem interface [Windows Shell], IDelegateItem interface [Windows Shell],described, _shell_IDelegateItem, shell.IDelegateItem, shobjidl_core/IDelegateItem
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDelegateItem
 - shobjidl_core/IDelegateItem
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
 - IDelegateItem
---

# IDelegateItem interface


## -description

Used to obtain the immediately underlying representation of an item's path.

## -remarks

This interface provides only the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface for system-provided data objects is provided with Windows. Custom data sources that want to expose this information must implement the interface as part of their data object.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to uncovers a single level of aliasing. For instance, if you have the path of an item in the Documents library, this interface reveals the path of the item in the location that was added to the library. Whether this is the file system path depends on the nature of that original location. For a full recursion to the source item, use <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname">IIdentityName</a>.