---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.ItemPostPaint
title: INameSpaceTreeControlCustomDraw::ItemPostPaint
author: windows-sdk-content
description: Called after an item in the namespace tree control is drawn.
old-location: shell\INameSpaceTreeControlCustomDraw_ItemPostPaint.htm
old-project: shell
ms.assetid: 9da2af87-a961-4ca8-a512-fe508f2b2d79
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],ItemPostPaint method, INameSpaceTreeControlCustomDraw.ItemPostPaint, INameSpaceTreeControlCustomDraw::ItemPostPaint, ItemPostPaint, ItemPostPaint method [Windows Shell], ItemPostPaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_ItemPostPaint, shell.INameSpaceTreeControlCustomDraw_ItemPostPaint, shobjidl/INameSpaceTreeControlCustomDraw::ItemPostPaint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlCustomDraw.ItemPostPaint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlCustomDraw::ItemPostPaint


## -description


Called after an item in the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the bounding rectangle of the area being drawn.


### -param pnstccdItem [in]

Type: <b><a href="https://msdn.microsoft.com/95747075-4882-4c29-8653-941ac04db54b">NSTCCUSTOMDRAW</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/95747075-4882-4c29-8653-941ac04db54b">NSTCCUSTOMDRAW</a> struct that determines the details of the drawing.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

