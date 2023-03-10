---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.ItemPrePaint
title: INameSpaceTreeControlCustomDraw::ItemPrePaint (shobjidl.h)
description: Called before an item in the namespace tree control is drawn.
helpviewer_keywords: ["INameSpaceTreeControlCustomDraw interface [Windows Shell]","ItemPrePaint method","INameSpaceTreeControlCustomDraw.ItemPrePaint","INameSpaceTreeControlCustomDraw::ItemPrePaint","ItemPrePaint","ItemPrePaint method [Windows Shell]","ItemPrePaint method [Windows Shell]","INameSpaceTreeControlCustomDraw interface","_shell_INameSpaceTreeControlCustomDraw_ItemPrePaint","shell.INameSpaceTreeControlCustomDraw_ItemPrePaint","shobjidl/INameSpaceTreeControlCustomDraw::ItemPrePaint"]
old-location: shell\INameSpaceTreeControlCustomDraw_ItemPrePaint.htm
tech.root: shell
ms.assetid: 0245ecfd-2617-481a-9d34-8fc4eb0ea012
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],ItemPrePaint method, INameSpaceTreeControlCustomDraw.ItemPrePaint, INameSpaceTreeControlCustomDraw::ItemPrePaint, ItemPrePaint, ItemPrePaint method [Windows Shell], ItemPrePaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_ItemPrePaint, shell.INameSpaceTreeControlCustomDraw_ItemPrePaint, shobjidl/INameSpaceTreeControlCustomDraw::ItemPrePaint
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControlCustomDraw::ItemPrePaint
 - shobjidl/INameSpaceTreeControlCustomDraw::ItemPrePaint
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
 - INameSpaceTreeControlCustomDraw.ItemPrePaint
---

# INameSpaceTreeControlCustomDraw::ItemPrePaint


## -description

Called before an item in the namespace tree control is drawn.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the bounding rectangle of the area being drawn.

### -param pnstccdItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ns-shobjidl-nstccustomdraw">NSTCCUSTOMDRAW</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl/ns-shobjidl-nstccustomdraw">NSTCCUSTOMDRAW</a> structure that determines the details of the drawing.

### -param pclrText [in, out]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

On entry, a pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure that declares the default color of the text. When this method returns, contains a pointer to a <b>COLORREF</b> structure that declares the color that should be used in its place, if any. This allows the client to provide their own color if they do not want to use the default.

### -param pclrTextBk [in, out]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

On entry, a pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure that declares the default color of the background. When this method returns, contains a pointer to a <b>COLORREF</b> structure that declares the color that should be used in its place, if any. This allows the client to provide their own color if they do not want to use the default.

### -param plres [out]

Type: <b>LRESULT*</b>

When this method returns, contains a pointer to an <b>LRESULT</b>, which points to one or more of the values from the <a href="/windows/desktop/Controls/cdrf-constants">CDRF Constants</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw">INameSpaceTreeControlCustomDraw</a>