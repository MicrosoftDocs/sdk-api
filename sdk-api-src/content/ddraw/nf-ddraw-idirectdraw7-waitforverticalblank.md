---
UID: NF:ddraw.IDirectDraw7.WaitForVerticalBlank
title: IDirectDraw7::WaitForVerticalBlank (ddraw.h)
author: windows-sdk-content
description: Helps the application synchronize itself with the vertical-blank interval.
old-location: directdraw\idirectdraw7_waitforverticalblank.htm
tech.root: directdraw
ms.assetid: ea52805d-201d-4fbe-a99f-5c04b7d620b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDWAITVB_BLOCKBEGIN, DDWAITVB_BLOCKBEGINEVENT, DDWAITVB_BLOCKEND, IDirectDraw7 interface [DirectDraw],WaitForVerticalBlank method, IDirectDraw7.WaitForVerticalBlank, IDirectDraw7::WaitForVerticalBlank, WaitForVerticalBlank, WaitForVerticalBlank method [DirectDraw], WaitForVerticalBlank method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::WaitForVerticalBlank, directdraw.idirectdraw7_waitforverticalblank
ms.topic: method
f1_keywords: 
 - "ddraw/IDirectDraw7.WaitForVerticalBlank"
dev_langs:
 - c++
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.WaitForVerticalBlank
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDraw7::WaitForVerticalBlank


## -description


Helps the application synchronize itself with the vertical-blank interval.


## -parameters




### -param arg1 [in]

One of the following flags that indicates how long to wait for the vertical blank:



#### DDWAITVB_BLOCKBEGIN

<b>WaitForVerticalBlank</b> returns when the vertical-blank interval begins.



#### DDWAITVB_BLOCKBEGINEVENT

Triggers an event when the vertical blank begins. This value is not currently supported.



#### DDWAITVB_BLOCKEND

<b>WaitForVerticalBlank</b> returns when the vertical-blank interval ends and the display begins.


### -param arg2 [in]

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



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>WaitForVerticalBlank</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
 

 

