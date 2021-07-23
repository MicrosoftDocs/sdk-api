---
UID: NF:shobjidl_core.IDragSourceHelper.InitializeFromBitmap
title: IDragSourceHelper::InitializeFromBitmap (shobjidl_core.h)
description: Initializes the drag-image manager for a windowless control.
helpviewer_keywords: ["IDragSourceHelper interface [Windows Shell]","InitializeFromBitmap method","IDragSourceHelper.InitializeFromBitmap","IDragSourceHelper::InitializeFromBitmap","InitializeFromBitmap","InitializeFromBitmap method [Windows Shell]","InitializeFromBitmap method [Windows Shell]","IDragSourceHelper interface","_win32_IDragSourceHelper_InitializeFromBitmap","shell.IDragSourceHelper_InitializeFromBitmap","shobjidl_core/IDragSourceHelper::InitializeFromBitmap"]
old-location: shell\IDragSourceHelper_InitializeFromBitmap.htm
tech.root: shell
ms.assetid: d50be9c9-f407-4386-bb8f-04c849205359
ms.date: 12/05/2018
ms.keywords: IDragSourceHelper interface [Windows Shell],InitializeFromBitmap method, IDragSourceHelper.InitializeFromBitmap, IDragSourceHelper::InitializeFromBitmap, InitializeFromBitmap, InitializeFromBitmap method [Windows Shell], InitializeFromBitmap method [Windows Shell],IDragSourceHelper interface, _win32_IDragSourceHelper_InitializeFromBitmap, shell.IDragSourceHelper_InitializeFromBitmap, shobjidl_core/IDragSourceHelper::InitializeFromBitmap
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDragSourceHelper::InitializeFromBitmap
 - shobjidl_core/IDragSourceHelper::InitializeFromBitmap
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
 - IDragSourceHelper.InitializeFromBitmap
---

# IDragSourceHelper::InitializeFromBitmap


## -description

Initializes the drag-image manager for a windowless control.

## -parameters

### -param pshdi [in]

Type: <b>LPSHDRAGIMAGE</b>

The <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shdragimage">SHDRAGIMAGE</a> structure that contains information about the bitmap.

### -param pDataObject [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the data object's <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Because <b>InitializeFromBitmap</b> always performs the RGB multiplication step in calculating the alpha value, you should always pass a bitmap without premultiplied alpha blending. Note that no error will result from passing the method a bitmap with premultiplied alpha blending, but this method will multiply it again, doubling the resulting alpha value.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a>