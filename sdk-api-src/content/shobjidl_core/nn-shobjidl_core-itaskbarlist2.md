---
UID: NN:shobjidl_core.ITaskbarList2
title: ITaskbarList2 (shobjidl_core.h)
description: Extends the ITaskbarList interface by exposing a method to mark a window as a full-screen display.
helpviewer_keywords: ["ITaskbarList2","ITaskbarList2 interface [Windows Shell]","ITaskbarList2 interface [Windows Shell]","described","shell.ITaskbarList2","shell_ITaskbarList2","shobjidl_core/ITaskbarList2"]
old-location: shell\ITaskbarList2.htm
tech.root: shell
ms.assetid: 8af23586-349f-4d21-98cb-0aaa27a586ff
ms.date: 12/05/2018
ms.keywords: ITaskbarList2, ITaskbarList2 interface [Windows Shell], ITaskbarList2 interface [Windows Shell],described, shell.ITaskbarList2, shell_ITaskbarList2, shobjidl_core/ITaskbarList2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITaskbarList2
 - shobjidl_core/ITaskbarList2
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
 - ITaskbarList2
---

# ITaskbarList2 interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a> interface by exposing a method to mark a window as a full-screen display.

## -inheritance

The <b>ITaskbarList2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>. <b>ITaskbarList2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a> interface, from which it inherits.

The Shell also automatically attempts to detect full-screen applications, but it is not as reliable as using the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist2-markfullscreenwindow">ITaskbarList2::MarkFullscreenWindow</a> method.
