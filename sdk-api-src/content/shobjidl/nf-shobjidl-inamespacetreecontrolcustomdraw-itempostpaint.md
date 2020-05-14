---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.ItemPostPaint
title: INameSpaceTreeControlCustomDraw::ItemPostPaint (shobjidl.h)
description: Called after an item in the namespace tree control is drawn.helpviewer_keywords: ["INameSpaceTreeControlCustomDraw interface [Windows Shell]","ItemPostPaint method","INameSpaceTreeControlCustomDraw.ItemPostPaint","INameSpaceTreeControlCustomDraw::ItemPostPaint","ItemPostPaint","ItemPostPaint method [Windows Shell]","ItemPostPaint method [Windows Shell]","INameSpaceTreeControlCustomDraw interface","_shell_INameSpaceTreeControlCustomDraw_ItemPostPaint","shell.INameSpaceTreeControlCustomDraw_ItemPostPaint","shobjidl/INameSpaceTreeControlCustomDraw::ItemPostPaint"]
old-location: shell\INameSpaceTreeControlCustomDraw_ItemPostPaint.htm
tech.root: shell
ms.assetid: 9da2af87-a961-4ca8-a512-fe508f2b2d79
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],ItemPostPaint method, INameSpaceTreeControlCustomDraw.ItemPostPaint, INameSpaceTreeControlCustomDraw::ItemPostPaint, ItemPostPaint, ItemPostPaint method [Windows Shell], ItemPostPaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_ItemPostPaint, shell.INameSpaceTreeControlCustomDraw_ItemPostPaint, shobjidl/INameSpaceTreeControlCustomDraw::ItemPostPaint
f1_keywords:
- shobjidl/INameSpaceTreeControlCustomDraw.ItemPostPaint
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- INameSpaceTreeControlCustomDraw.ItemPostPaint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlCustomDraw::ItemPostPaint


## -description


Called after an item in the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the bounding rectangle of the area being drawn.


### -param pnstccdItem [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ns-shobjidl-nstccustomdraw">NSTCCUSTOMDRAW</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ns-shobjidl-nstccustomdraw">NSTCCUSTOMDRAW</a> struct that determines the details of the drawing.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw">INameSpaceTreeControlCustomDraw</a>
 

 

