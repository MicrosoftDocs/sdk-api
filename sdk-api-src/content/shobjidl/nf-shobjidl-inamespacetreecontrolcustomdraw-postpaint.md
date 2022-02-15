---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.PostPaint
title: INameSpaceTreeControlCustomDraw::PostPaint (shobjidl.h)
description: Called after the namespace tree control is drawn.
helpviewer_keywords: ["INameSpaceTreeControlCustomDraw interface [Windows Shell]","PostPaint method","INameSpaceTreeControlCustomDraw.PostPaint","INameSpaceTreeControlCustomDraw::PostPaint","PostPaint","PostPaint method [Windows Shell]","PostPaint method [Windows Shell]","INameSpaceTreeControlCustomDraw interface","_shell_INameSpaceTreeControlCustomDraw_PostPaint","shell.INameSpaceTreeControlCustomDraw_PostPaint","shobjidl/INameSpaceTreeControlCustomDraw::PostPaint"]
old-location: shell\INameSpaceTreeControlCustomDraw_PostPaint.htm
tech.root: shell
ms.assetid: fe8cedc8-166d-4802-9d01-7c3991181618
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],PostPaint method, INameSpaceTreeControlCustomDraw.PostPaint, INameSpaceTreeControlCustomDraw::PostPaint, PostPaint, PostPaint method [Windows Shell], PostPaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_PostPaint, shell.INameSpaceTreeControlCustomDraw_PostPaint, shobjidl/INameSpaceTreeControlCustomDraw::PostPaint
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
 - INameSpaceTreeControlCustomDraw::PostPaint
 - shobjidl/INameSpaceTreeControlCustomDraw::PostPaint
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
 - INameSpaceTreeControlCustomDraw.PostPaint
---

# INameSpaceTreeControlCustomDraw::PostPaint


## -description

Called after the namespace tree control is drawn.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.

### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the bounding rectangle of the area being drawn.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw">INameSpaceTreeControlCustomDraw</a>