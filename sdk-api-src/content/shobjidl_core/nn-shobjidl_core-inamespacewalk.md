---
UID: NN:shobjidl_core.INamespaceWalk
title: INamespaceWalk (shobjidl_core.h)
description: Exposes methods that walk a namespace from a given root node. The depth of the walk is specified and an optional array is returned containing the IDs of all nodes walked.
helpviewer_keywords: ["INamespaceWalk","INamespaceWalk interface [Windows Shell]","INamespaceWalk interface [Windows Shell]","described","_win32_INamespaceWalk","shell.INamespaceWalk","shobjidl_core/INamespaceWalk"]
old-location: shell\INamespaceWalk.htm
tech.root: shell
ms.assetid: 164732ae-1c72-465c-a16b-a8eeaa9cc185
ms.date: 12/05/2018
ms.keywords: INamespaceWalk, INamespaceWalk interface [Windows Shell], INamespaceWalk interface [Windows Shell],described, _win32_INamespaceWalk, shell.INamespaceWalk, shobjidl_core/INamespaceWalk
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INamespaceWalk
 - shobjidl_core/INamespaceWalk
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
 - INamespaceWalk
---

# INamespaceWalk interface


## -description

Exposes methods that walk a namespace from a given root node. The depth of the walk is specified and an optional array is returned containing the IDs of all nodes walked.

## -inheritance

The <b>INamespaceWalk</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamespaceWalk</b> also has these types of members:

## -remarks

Use this interface to display or perform an operation on the contents of the namespace. <b>INamespaceWalk</b> allows retrieval of all reachable nodes of your namespace as pointers to item identifier lists (PIDLs), which can in turn be used to retrieve the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object for each.

The class identifier (CLSID) for the default implementation of <b>INamespaceWalk</b> is CLSID_NamespaceWalker. You can obtain an <b>INamespaceWalk</b> object by creating a single uninitialized object of the class associated with CLSID_NamespaceWalker using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. This interface's IID is IID_INamespaceWalk.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a>
