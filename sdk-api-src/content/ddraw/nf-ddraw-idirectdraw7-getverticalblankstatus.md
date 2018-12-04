---
UID: NF:ddraw.IDirectDraw7.GetVerticalBlankStatus
title: IDirectDraw7::GetVerticalBlankStatus
author: windows-sdk-content
description: Retrieves the status of the vertical blank.
old-location: directdraw\idirectdraw7_getverticalblankstatus.htm
tech.root: directdraw
ms.assetid: 4bab0d24-ab11-46fb-92de-060f6afe1fde
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetVerticalBlankStatus, GetVerticalBlankStatus method [DirectDraw], GetVerticalBlankStatus method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetVerticalBlankStatus method, IDirectDraw7.GetVerticalBlankStatus, IDirectDraw7::GetVerticalBlankStatus, ddraw/IDirectDraw7::GetVerticalBlankStatus, directdraw.idirectdraw7_getverticalblankstatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectDraw7.GetVerticalBlankStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::GetVerticalBlankStatus


## -description


Retrieves the status of the vertical blank.


## -parameters






#### - lpbIsInVB [out]

A pointer to a variable that receives the status of the vertical blank. This parameter is TRUE if a vertical blank is occurring, and FALSE otherwise.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



To synchronize with the vertical blank, use the <a href="https://msdn.microsoft.com/ea52805d-201d-4fbe-a99f-5c04b7d620b5">IDirectDraw7::WaitForVerticalBlank</a> method.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>GetVerticalBlankStatus</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

