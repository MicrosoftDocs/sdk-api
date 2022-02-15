---
UID: NN:shobjidl.IDragSourceHelper2
title: IDragSourceHelper2 (shobjidl.h)
description: Exposes a method that adds functionality to IDragSourceHelper. This method sets the characteristics of a drag-and-drop operation over an IDragSourceHelper object.
helpviewer_keywords: ["IDragSourceHelper2","IDragSourceHelper2 interface [Windows Shell]","IDragSourceHelper2 interface [Windows Shell]","described","_shell_IDragSourceHelper2","shell.IDragSourceHelper2","shobjidl/IDragSourceHelper2"]
old-location: shell\IDragSourceHelper2.htm
tech.root: shell
ms.assetid: 20529b27-22d2-4c77-a2a7-93e54b0b7748
ms.date: 12/05/2018
ms.keywords: IDragSourceHelper2, IDragSourceHelper2 interface [Windows Shell], IDragSourceHelper2 interface [Windows Shell],described, _shell_IDragSourceHelper2, shell.IDragSourceHelper2, shobjidl/IDragSourceHelper2
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDragSourceHelper2
 - shobjidl/IDragSourceHelper2
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
 - IDragSourceHelper2
---

# IDragSourceHelper2 interface


## -description

Exposes a method that adds functionality to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a>. This method sets the characteristics of a drag-and-drop operation over an <b>IDragSourceHelper</b> object.

## -inheritance

The <b>IDragSourceHelper2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a>. <b>IDragSourceHelper2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a> interface, from which it inherits.

If you want to adjust the behavior of the drag image by calling <a href="/windows/desktop/api/shobjidl/nf-shobjidl-idragsourcehelper2-setflags">IDragSourceHelper2::SetFlags</a>, that call should be made before you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow">InitializeFromWindow</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap">InitializeFromBitmap</a>.
