---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.ItemPrePaint
title: INameSpaceTreeControlCustomDraw::ItemPrePaint
author: windows-sdk-content
description: Called before an item in the namespace tree control is drawn.
old-location: shell\INameSpaceTreeControlCustomDraw_ItemPrePaint.htm
old-project: shell
ms.assetid: 0245ecfd-2617-481a-9d34-8fc4eb0ea012
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],ItemPrePaint method, INameSpaceTreeControlCustomDraw.ItemPrePaint, INameSpaceTreeControlCustomDraw::ItemPrePaint, ItemPrePaint, ItemPrePaint method [Windows Shell], ItemPrePaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_ItemPrePaint, shell.INameSpaceTreeControlCustomDraw_ItemPrePaint, shobjidl/INameSpaceTreeControlCustomDraw::ItemPrePaint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - INameSpaceTreeControlCustomDraw.ItemPrePaint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlCustomDraw::ItemPrePaint


## -description


Called before an item in the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that describes the bounding rectangle of the area being drawn.


### -param pnstccdItem [in]

Type: <b><a href="https://msdn.microsoft.com/95747075-4882-4c29-8653-941ac04db54b">NSTCCUSTOMDRAW</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/95747075-4882-4c29-8653-941ac04db54b">NSTCCUSTOMDRAW</a> structure that determines the details of the drawing.


### -param pclrText [in, out]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

On entry, a pointer to a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that declares the default color of the text. When this method returns, contains a pointer to a <b>COLORREF</b> structure that declares the color that should be used in its place, if any. This allows the client to provide their own color if they do not want to use the default.


### -param pclrTextBk [in, out]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

On entry, a pointer to a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that declares the default color of the background. When this method returns, contains a pointer to a <b>COLORREF</b> structure that declares the color that should be used in its place, if any. This allows the client to provide their own color if they do not want to use the default.


### -param plres [out]

Type: <b>LRESULT*</b>

When this method returns, contains a pointer to an <b>LRESULT</b>, which points to one or more of the values from the <a href="https://msdn.microsoft.com/library/Bb775489(v=VS.85).aspx">CDRF Constants</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

