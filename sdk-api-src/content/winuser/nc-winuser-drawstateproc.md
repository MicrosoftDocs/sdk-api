---
UID: NC:winuser.DRAWSTATEPROC
title: DRAWSTATEPROC (winuser.h)
author: windows-sdk-content
description: The DrawStateProc function is an application-defined callback function that renders a complex image for the DrawState function.
old-location: gdi\drawstateproc.htm
tech.root: gdi
ms.assetid: a95a4020-e433-4b2c-96e7-f272e28e5a43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawStateProc, DrawStateProc callback, DrawStateProc callback function [Windows GDI], _win32_DrawStateProc, gdi.drawstateproc, winuser/DrawStateProc
ms.topic: callback
f1_keywords: 
 - "winuser/DrawStateProc"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - DrawStateProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DRAWSTATEPROC callback function


## -description


The <b>DrawStateProc</b> function is an application-defined callback function that renders a complex image for the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a> function. The <b>DRAWSTATEPROC</b> type defines a pointer to this callback function. <b>DrawStateProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param hdc [in]

A handle to the device context to draw in. The device context is a memory device context with a bitmap selected, the dimensions of which are at least as great as those specified by the <i>cx</i> and <i>cy</i> parameters.


### -param lData [in]

Specifies information about the image, which the application passed to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a>.


### -param wData [in]

Specifies information about the image, which the application passed to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a>.


### -param cx [in]

The image width, in device units, as specified by the call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a>.


### -param cy [in]

The image height, in device units, as specified by the call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-drawstatea">DrawState</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>
 

 

