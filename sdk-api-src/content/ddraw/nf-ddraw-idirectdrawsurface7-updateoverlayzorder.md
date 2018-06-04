---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirectDrawSurface7::UpdateOverlayZOrder


## -description


Sets the z-order of an overlay.


## -parameters




### -param






#### - dwFlags [in]

One of the following flags that determines the z-order of the overlay:



#### DDOVERZ_INSERTINBACKOF

Inserts this overlay in the overlay chain behind the reference overlay.



#### DDOVERZ_INSERTINFRONTOF

Inserts this overlay in the overlay chain in front of the reference overlay.



#### DDOVERZ_MOVEBACKWARD

Moves this overlay one position backward in the overlay chain.



#### DDOVERZ_MOVEFORWARD

Moves this overlay one position forward in the overlay chain.



#### DDOVERZ_SENDTOBACK

Moves this overlay to the back of the overlay chain.



#### DDOVERZ_SENDTOFRONT

Moves this overlay to the front of the overlay chain.


#### - lpDDSReference [in]

A pointer to the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the DirectDraw surface to be used as a relative position in the overlay chain. This parameter is needed only for the DDOVERZ_INSERTINBACKOF and DDOVERZ_INSERTINFRONTOF flags.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>UpdateOverlayZOrder</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

