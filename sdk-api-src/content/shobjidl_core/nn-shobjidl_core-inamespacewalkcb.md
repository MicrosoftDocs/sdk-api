---
UID: NN:shobjidl_core.INamespaceWalkCB
title: INamespaceWalkCB (shobjidl_core.h)
description: A callback interface exposing methods used with INamespaceWalk.
helpviewer_keywords: ["INamespaceWalkCB","INamespaceWalkCB interface [Windows Shell]","INamespaceWalkCB interface [Windows Shell]","described","_win32_INamespaceWalkCB","shell.INamespaceWalkCB","shobjidl_core/INamespaceWalkCB"]
old-location: shell\INamespaceWalkCB.htm
tech.root: shell
ms.assetid: 15244d6e-6cd7-4dee-8e4e-2533d5a60ae7
ms.date: 12/05/2018
ms.keywords: INamespaceWalkCB, INamespaceWalkCB interface [Windows Shell], INamespaceWalkCB interface [Windows Shell],described, _win32_INamespaceWalkCB, shell.INamespaceWalkCB, shobjidl_core/INamespaceWalkCB
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
 - INamespaceWalkCB
 - shobjidl_core/INamespaceWalkCB
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
 - INamespaceWalkCB
---

# INamespaceWalkCB interface


## -description

A callback interface exposing methods used with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>. After performing a walk with <b>INamespaceWalk</b>, an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object representing the walked nodes is passed to the <b>INamespaceWalkCB</b> methods. What those methods do with the information depends on the object that is implementing them.

## -inheritance

The <b>INamespaceWalkCB</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamespaceWalkCB</b> also has these types of members:

## -remarks

The IID for this interface is IID_INamespaceWalkCB.
