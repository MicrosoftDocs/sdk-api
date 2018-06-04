---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

When this method returns, contains a pointer to an <b>LRESULT</b>, which points to one or more of the values from the <a href="https://msdn.microsoft.com/6b05e27e-5d18-46f2-b326-2a5148597852">CDRF Constants</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

