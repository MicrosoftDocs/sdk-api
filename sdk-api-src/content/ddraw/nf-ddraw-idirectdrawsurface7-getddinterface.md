---
UID: NF:ddraw.IDirectDrawSurface7.GetDDInterface
title: IDirectDrawSurface7::GetDDInterface
author: windows-sdk-content
description: Retrieves an interface to the DirectDraw object that was used to create this surface.
old-location: directdraw\idirectdrawsurface7_getddinterface.htm
tech.root: directdraw
ms.assetid: 1ec63614-cdc0-4d07-97e3-97167e7b397c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDDInterface, GetDDInterface method [DirectDraw], GetDDInterface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetDDInterface method, IDirectDrawSurface7.GetDDInterface, IDirectDrawSurface7::GetDDInterface, ddraw/IDirectDrawSurface7::GetDDInterface, directdraw.idirectdrawsurface7_getddinterface
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
 - IDirectDrawSurface7.GetDDInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetDDInterface


## -description


Retrieves an interface to the DirectDraw object that was used to create this surface.


## -parameters






#### - lplpDD [out]

A pointer to a variable that receives a valid interface pointer if the call succeeds. Cast this pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer; then query for the <a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a> interface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetDDInterface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

