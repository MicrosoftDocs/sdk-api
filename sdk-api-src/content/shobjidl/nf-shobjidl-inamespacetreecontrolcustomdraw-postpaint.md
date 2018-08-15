---
UID: NF:shobjidl.INameSpaceTreeControlCustomDraw.PostPaint
title: INameSpaceTreeControlCustomDraw::PostPaint
author: windows-sdk-content
description: Called after the namespace tree control is drawn.
old-location: shell\INameSpaceTreeControlCustomDraw_PostPaint.htm
old-project: shell
ms.assetid: fe8cedc8-166d-4802-9d01-7c3991181618
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INameSpaceTreeControlCustomDraw interface [Windows Shell],PostPaint method, INameSpaceTreeControlCustomDraw.PostPaint, INameSpaceTreeControlCustomDraw::PostPaint, PostPaint, PostPaint method [Windows Shell], PostPaint method [Windows Shell],INameSpaceTreeControlCustomDraw interface, _shell_INameSpaceTreeControlCustomDraw_PostPaint, shell.INameSpaceTreeControlCustomDraw_PostPaint, shobjidl/INameSpaceTreeControlCustomDraw::PostPaint
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
 - INameSpaceTreeControlCustomDraw.PostPaint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlCustomDraw::PostPaint


## -description


Called after the namespace tree control is drawn.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

A handle to the control's device context. Use this HDC to perform any GDI functions.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that describes the bounding rectangle of the area being drawn.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e">INameSpaceTreeControlCustomDraw</a>
 

 

