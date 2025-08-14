---
UID: NF:ole2.OleSetMenuDescriptor
title: OleSetMenuDescriptor function (ole2.h)
description: Installs or removes OLE dispatching code from the container's frame window.
helpviewer_keywords: ["OleSetMenuDescriptor","OleSetMenuDescriptor function [COM]","_ole_OleSetMenuDescriptor","com.olesetmenudescriptor","ole2/OleSetMenuDescriptor"]
old-location: com\olesetmenudescriptor.htm
tech.root: com
ms.assetid: c80fe36d-5093-4814-83a9-0c11c5a7cf5f
ms.date: 12/05/2018
ms.keywords: OleSetMenuDescriptor, OleSetMenuDescriptor function [COM], _ole_OleSetMenuDescriptor, com.olesetmenudescriptor, ole2/OleSetMenuDescriptor
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleSetMenuDescriptor
 - ole2/OleSetMenuDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - OleSetMenuDescriptor
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# OleSetMenuDescriptor function


## -description

Installs or removes OLE dispatching code from the container's frame window.

## -parameters

### -param holemenu [in]

Handle to the composite menu descriptor returned by the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a> function. If <b>NULL</b>, the dispatching code is unhooked.

### -param hwndFrame [in]

 Handle to the container's frame window where the in-place composite menu is to be installed.

### -param hwndActiveObject [in]

Handle to the object's in-place activation window. OLE dispatches menu messages and commands to this window.

### -param lpFrame [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceframe">IOleInPlaceFrame</a> interface on the container's frame window.

### -param lpActiveObj [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a> interface on the active in-place object.

## -returns

This function returns S_OK on success.

## -remarks

The container should call <b>OleSetMenuDescriptor</b> to install the dispatching code on <i>hwndFrame</i> when the object calls the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a> method, or to remove the dispatching code by passing <b>NULL</b> as the value for <i>holemenu</i> to <b>OleSetMenuDescriptor</b>.

If both the <i>lpFrame</i> and <i>lpActiveObj</i> parameters are non-<b>NULL</b>, OLE installs the context-sensitive help F1 message filter for the application. Otherwise, the application must supply its own message filter.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatemenudescriptor">OleCreateMenuDescriptor</a>
