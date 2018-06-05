---
UID: NF:ddraw.IDirectDraw7.GetScanLine
title: IDirectDraw7::GetScanLine
author: windows-sdk-content
description: Retrieves the scan line that is currently being drawn on the monitor.
old-location: directdraw\idirectdraw7_getscanline.htm
old-project: directdraw
ms.assetid: 0bccb384-2de3-49a5-962a-31ad2a751e28
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetScanLine, GetScanLine method [DirectDraw], GetScanLine method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetScanLine method, IDirectDraw7.GetScanLine, IDirectDraw7::GetScanLine, ddraw/IDirectDraw7::GetScanLine, directdraw.idirectdraw7_getscanline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDraw7.GetScanLine
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::GetScanLine


## -description


Retrieves the scan line that is currently being drawn on the monitor.


## -parameters






#### - lpdwScanLine [out]

A pointer to a variable that receives the scan line that the display is currently drawing.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_VERTICALBLANKINPROGRESS</li>
</ul>



## -remarks



Scan lines are reported as zero-based integers. The returned scan line value is in the range from 0 through n, where 0 is the first visible scan line on the screen and n is the last visible scan line, plus any scan lines that occur during the vertical blank period. So, in a case where an application is running at a resolution of 640×480 and there are 12 scan lines during vblank, the values returned by this method range from 0 through 491.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <a href="https://msdn.microsoft.com/13f8e5c2-b957-43ce-9fc8-5554c2321bdd">GetMonitorFrequency</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

