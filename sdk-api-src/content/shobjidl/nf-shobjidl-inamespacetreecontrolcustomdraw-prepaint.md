---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.PrePaint
title: INameSpaceTreeControlCustomDraw::PrePaint (shobjidl.h)
description: Called before the namespace tree control is drawn.
helpviewer_keywords: ["INameSpaceTreeControlCustomDraw interface [Windows Shell]","PrePaint method","INameSpaceTreeControlCustomDraw.PrePaint","INameSpaceTreeControlCustomDraw::PrePaint","PrePaint","PrePaint method [Windows Shell]","PrePaint method [Windows Shell]","INameSpaceTreeControlCustomDraw interface","_shell_INameSpaceTreeControlCustomDraw_PrePaint","shell.INameSpaceTreeControlCustomDraw_PrePaint","shobjidl/INameSpaceTreeControlCustomDraw::PrePaint"]
old-location: shell\INameSpaceTreeControlCustomDraw_PrePaint.htm
tech.root: shell
ms.assetid: 3d9c0616-90f2-435c-a663-9ffe4adab8a0
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],PrePaint method, INameSpaceTreeControlCustomDraw.PrePaint, INameSpaceTreeControlCustomDraw::PrePaint, PrePaint, PrePaint method [Windows Shell], PrePaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_PrePaint, shell.INameSpaceTreeControlCustomDraw_PrePaint, shobjidl/INameSpaceTreeControlCustomDraw::PrePaint
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
 - INameSpaceTreeControlCustomDraw::PrePaint
 - shobjidl/INameSpaceTreeControlCustomDraw::PrePaint
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
 - INameSpaceTreeControlCustomDraw.PrePaint
---

# INameSpaceTreeControlCustomDraw::PrePaint


## -description

Called before the namespace tree control is drawn.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the bounding rectangle of the area being drawn.

### -param plres [out]

Type: <b>LRESULT*</b>

When this method returns, contains a pointer to an <b>LRESULT</b>, which contains one or more of the values from the <a href="/windows/desktop/Controls/cdrf-constants">CDRF Constants</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw">INameSpaceTreeControlCustomDraw</a>