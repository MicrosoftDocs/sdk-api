---
UID: NF:ddraw.IDirectDraw7.GetMonitorFrequency
title: IDirectDraw7::GetMonitorFrequency
author: windows-sdk-content
description: Retrieves the frequency of the monitor that the DirectDraw object controls.
old-location: directdraw\idirectdraw7_getmonitorfrequency.htm
tech.root: directdraw
ms.assetid: 13f8e5c2-b957-43ce-9fc8-5554c2321bdd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMonitorFrequency, GetMonitorFrequency method [DirectDraw], GetMonitorFrequency method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetMonitorFrequency method, IDirectDraw7.GetMonitorFrequency, IDirectDraw7::GetMonitorFrequency, ddraw/IDirectDraw7::GetMonitorFrequency, directdraw.idirectdraw7_getmonitorfrequency
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
 - IDirectDraw7.GetMonitorFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::GetMonitorFrequency


## -description


Retrieves the frequency of the monitor that the DirectDraw object controls.


## -parameters






#### - lpdwFrequency [out]

A pointer to a variable that receives the monitor frequency, in Hz.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>GetMonitorFrequency</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

