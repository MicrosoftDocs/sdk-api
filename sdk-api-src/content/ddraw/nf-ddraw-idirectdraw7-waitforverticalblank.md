---
UID: NF:ddraw.IDirectDraw7.WaitForVerticalBlank
title: IDirectDraw7::WaitForVerticalBlank
author: windows-sdk-content
description: Helps the application synchronize itself with the vertical-blank interval.
old-location: directdraw\idirectdraw7_waitforverticalblank.htm
old-project: directdraw
ms.assetid: ea52805d-201d-4fbe-a99f-5c04b7d620b5
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DDWAITVB_BLOCKBEGIN, DDWAITVB_BLOCKBEGINEVENT, DDWAITVB_BLOCKEND, IDirectDraw7 interface [DirectDraw],WaitForVerticalBlank method, IDirectDraw7.WaitForVerticalBlank, IDirectDraw7::WaitForVerticalBlank, WaitForVerticalBlank, WaitForVerticalBlank method [DirectDraw], WaitForVerticalBlank method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::WaitForVerticalBlank, directdraw.idirectdraw7_waitforverticalblank
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDraw7.WaitForVerticalBlank
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::WaitForVerticalBlank


## -description


Helps the application synchronize itself with the vertical-blank interval.


## -parameters




### -param






#### - dwFlags [in]

One of the following flags that indicates how long to wait for the vertical blank:



#### DDWAITVB_BLOCKBEGIN

<b>WaitForVerticalBlank</b> returns when the vertical-blank interval begins.



#### DDWAITVB_BLOCKBEGINEVENT

Triggers an event when the vertical blank begins. This value is not currently supported.



#### DDWAITVB_BLOCKEND

<b>WaitForVerticalBlank</b> returns when the vertical-blank interval ends and the display begins.


#### - hEvent [in]

Handle of the event to be triggered when the vertical blank begins. This parameter is not currently used.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>WaitForVerticalBlank</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

