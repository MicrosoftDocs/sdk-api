---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.PrePaint
title: INameSpaceTreeControlCustomDraw::PrePaint
author: windows-sdk-content
description: Called before the namespace tree control is drawn.
old-location: shell\INameSpaceTreeControlCustomDraw_PrePaint.htm
tech.root: Shell
ms.assetid: 3d9c0616-90f2-435c-a663-9ffe4adab8a0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],PrePaint method, INameSpaceTreeControlCustomDraw.PrePaint, INameSpaceTreeControlCustomDraw::PrePaint, PrePaint, PrePaint method [Windows Shell], PrePaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_PrePaint, shell.INameSpaceTreeControlCustomDraw_PrePaint, shobjidl/INameSpaceTreeControlCustomDraw::PrePaint
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INameSpaceTreeControlCustomDraw.PrePaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlCustomDraw::PrePaint


## -description


Called before the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the bounding rectangle of the area being drawn.


### -param plres [out]

Type: <b>LRESULT*</b>

When this method returns, contains a pointer to an <b>LRESULT</b>, which contains one or more of the values from the <a href="https://msdn.microsoft.com/en-us/library/Bb775489(v=VS.85).aspx">CDRF Constants</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

