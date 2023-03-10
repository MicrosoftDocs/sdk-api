---
UID: NN:shobjidl.INameSpaceTreeControl2
title: INameSpaceTreeControl2 (shobjidl.h)
description: Extends the INameSpaceTreeControl interface by providing methods that get and set the display styles of treeview controls for use with Shell namespace items.
helpviewer_keywords: ["INameSpaceTreeControl2","INameSpaceTreeControl2 interface [Windows Shell]","INameSpaceTreeControl2 interface [Windows Shell]","described","_shell_INameSpaceTreeControl2","shell.INameSpaceTreeControl2","shobjidl/INameSpaceTreeControl2"]
old-location: shell\INameSpaceTreeControl2.htm
tech.root: shell
ms.assetid: 5f9514db-35fe-44c7-9324-d69022628913
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl2, INameSpaceTreeControl2 interface [Windows Shell], INameSpaceTreeControl2 interface [Windows Shell],described, _shell_INameSpaceTreeControl2, shell.INameSpaceTreeControl2, shobjidl/INameSpaceTreeControl2
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControl2
 - shobjidl/INameSpaceTreeControl2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControl2
---

# INameSpaceTreeControl2 interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> interface by providing methods that get and set the display styles of treeview controls for use with Shell namespace items.

## -inheritance

The <b>INameSpaceTreeControl2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>. <b>INameSpaceTreeControl2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> interface, from which it inherits.

Use class identifier (CLSID) CLSID_NameSpaceTreeControl to instantiate an instance of this interface.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows. Third parties should not implement their own versions.
