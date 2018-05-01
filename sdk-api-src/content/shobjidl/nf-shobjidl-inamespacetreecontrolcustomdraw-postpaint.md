---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.PostPaint
title: INameSpaceTreeControlCustomDraw::PostPaint method
author: windows-driver-content
description: Called after the namespace tree control is drawn.
old-location: shell\INameSpaceTreeControlCustomDraw_PostPaint.htm
old-project: shell
ms.assetid: fe8cedc8-166d-4802-9d01-7c3991181618
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: INameSpaceTreeControlCustomDraw, INameSpaceTreeControlCustomDraw interface [Windows Shell], PostPaint method, INameSpaceTreeControlCustomDraw::PostPaint, PostPaint method [Windows Shell], PostPaint method [Windows Shell], INameSpaceTreeControlCustomDraw interface, PostPaint,INameSpaceTreeControlCustomDraw.PostPaint, _shell_INameSpaceTreeControlCustomDraw_PostPaint, shell.INameSpaceTreeControlCustomDraw_PostPaint, shobjidl/INameSpaceTreeControlCustomDraw::PostPaint
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	INameSpaceTreeControlCustomDraw.PostPaint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlCustomDraw::PostPaint method


## -description


Called after the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that describes the bounding rectangle of the area being drawn.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

