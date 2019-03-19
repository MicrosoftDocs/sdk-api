---
UID: NF:ddraw.IDirectDrawSurface7.ChangeUniquenessValue
title: IDirectDrawSurface7::ChangeUniquenessValue (ddraw.h)
author: windows-sdk-content
description: Manually updates the uniqueness value for this surface.
old-location: directdraw\idirectdrawsurface7_changeuniquenessvalue.htm
tech.root: directdraw
ms.assetid: 4d714fb7-7e12-45ab-ae40-7fc2a65b9e7e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ChangeUniquenessValue, ChangeUniquenessValue method [DirectDraw], ChangeUniquenessValue method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],ChangeUniquenessValue method, IDirectDrawSurface7.ChangeUniquenessValue, IDirectDrawSurface7::ChangeUniquenessValue, ddraw/IDirectDrawSurface7::ChangeUniquenessValue, directdraw.idirectdrawsurface7_changeuniquenessvalue
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
 - IDirectDrawSurface7.ChangeUniquenessValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::ChangeUniquenessValue


## -description


Manually updates the uniqueness value for this surface.



## -parameters






## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



DirectDraw automatically updates uniqueness values whenever the contents of a surface change.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>ChangeUniquenessValue</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

