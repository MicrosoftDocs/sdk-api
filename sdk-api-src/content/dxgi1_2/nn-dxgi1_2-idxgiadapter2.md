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

# IDXGIAdapter2 interface


## -description



        The <b>IDXGIAdapter2</b> interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter2</b> interface inherits from <a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a>. <b>IDXGIAdapter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC1A054D-4092-4865-A6EF-B936891AA470">GetDesc2</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.2 description of an adapter or video card. This description includes information about the granularity at which the GPU can be preempted from performing its current task.

</td>
</tr>
</table> 


## -remarks




          A display subsystem is often referred to as a video card; however, on some computers, the display subsystem is part of the motherboard.
        


          To enumerate the display subsystems, use <a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">IDXGIFactory1::EnumAdapters1</a>.
        


          To get an interface to the adapter for a particular device, use <a href="https://msdn.microsoft.com/ae113b36-47fd-4db1-b10c-ced22ec52435">IDXGIDevice::GetAdapter</a>.
        


          To create a software adapter, use <a href="https://msdn.microsoft.com/46c10086-aa57-42f6-a619-8c537e4ae406">IDXGIFactory::CreateSoftwareAdapter</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a>
 

 

