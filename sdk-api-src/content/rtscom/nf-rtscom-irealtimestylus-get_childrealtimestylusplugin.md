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

# IRealTimeStylus::get_ChildRealTimeStylusPlugin


## -description



Gets or sets a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object as an asynchronous plug-in of the current <b>RealTimeStylus</b> object.



This property is read/write.


## -parameters


## -remarks



If there is no child RTS, getting the property returns S_OK with the <i>ppiRTS</i> parameter set to <b>NULL</b>. Setting the child RTS property to <b>NULL</b> breaks the cascade.

<div class="alert"><b>Note</b>  If there is no child RTS, setting the property to <b>NULL</b> returns S_OK.</div>
<div> </div>
A child <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> cannot have another cascaded child <b>RealTimeStylus</b>.

Plug-ins in the asynchronous collection cannot have children.

If a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object is set as a child by using the <b>IRealTimeStylus::ChildRealTimeStylusPlugin Property</b> property, no other asynchronous plug-ins can be added to the parent <b>RealTimeStylus</b>. The depth and breadth of the chain is limited to one child <b>RealTimeStylus</b> object. A child <b>RealTimeStylus</b> can have asynchronous plug-ins.

With the exception of <a href="https://msdn.microsoft.com/45861b92-0a2c-42ec-96e5-c3afd45e0e85">IRealTimeStylus::GetStylusAsyncPluginCount Method</a>, the asynchronous plug-in methods, such as <a href="https://msdn.microsoft.com/fc22fa79-469a-47f0-96ce-9a041fc8a617">IRealTimeStylus::AddStylusAsyncPlugin Method</a>, return E_INVALIDOPERATION when called on a parent <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a>.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/229e14f6-e0b1-40e0-a58e-daf1ba08cd1f">IRealTimeStylus::GetStylusAsyncPlugin Method</a>



<a href="https://msdn.microsoft.com/98b97156-f181-45f4-9cfb-13816f8042e6">IRealTimeStylus::RemoveAllStylusAsyncPlugins Method</a>



<a href="https://msdn.microsoft.com/9c993147-3711-45ad-8996-e1434fd4b657">IRealTimeStylus::RemoveStylusAsyncPlugin Method</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

