---
UID: NF:ddraw.IDirectDraw7.RestoreDisplayMode
title: IDirectDraw7::RestoreDisplayMode (ddraw.h)
author: windows-sdk-content
description: Resets the mode of the display device hardware for the primary surface to what it was before the IDirectDraw7::SetDisplayMode method was called. Exclusive-level access is required to use this method.
old-location: directdraw\idirectdraw7_restoredisplaymode.htm
tech.root: directdraw
ms.assetid: 7538339a-8886-4b40-9779-17c8ebe81446
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],RestoreDisplayMode method, IDirectDraw7.RestoreDisplayMode, IDirectDraw7::RestoreDisplayMode, RestoreDisplayMode, RestoreDisplayMode method [DirectDraw], RestoreDisplayMode method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::RestoreDisplayMode, directdraw.idirectdraw7_restoredisplaymode
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
 - IDirectDraw7.RestoreDisplayMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::RestoreDisplayMode


## -description


Resets the mode of the display device hardware for the primary surface to what it was before the <a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">IDirectDraw7::SetDisplayMode</a> method was called. Exclusive-level access is required to use this method.



## -parameters






## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_LOCKEDSURFACES</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>RestoreDisplayMode</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

