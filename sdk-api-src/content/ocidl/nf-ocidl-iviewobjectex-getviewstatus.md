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

# IViewObjectEx::GetViewStatus


## -description


Retrieves information about the opacity of the object, and what drawing aspects are supported.


## -parameters




### -param pdwStatus [out]

A pointer to the view status. This information is returned as a combination of the <a href="https://msdn.microsoft.com/7b3118af-db29-4eb1-9b1b-38a8ebe42f19">VIEWSTATUS</a> enumeration values.


## -returns



This method returns S_OK on success.




## -remarks



In order to optimize the drawing process, the container needs to be able to determine whether an object is opaque and whether it has a solid background. It is not necessary to redraw objects that are entirely covered by a completely opaque object. Other operations, such as scrolling for example, can also be highly optimized if an object is opaque and has a solid background.

The <b>IViewObjectEx::GetViewStatus</b> method returns whether the object is entirely opaque or not (VIEWSTATUS_OPAQUE bit) and whether its background is solid (VIEWSTATUS_SOLIDBKGND bit). This information may change in time. An object may be opaque at a given time and become totally or partially transparent later on, for example, because of a change of the BackStyle property. An object should notify its sites when it changes using <a href="https://msdn.microsoft.com/9d5129aa-341c-4c69-8c0c-b7c3e62a57c1">IAdviseSinkEx::OnViewStatusChange</a> so the sites can cache this information for high speed access.

Objects not supporting <a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a> are considered to be always transparent.

The <b>IViewObjectEx::GetViewStatus</b> method also returns a combination of bits indicating which aspects are supported.

If a given drawing aspect is not supported, all <a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a> methods taking a drawing aspect as an input parameter should fail and return E_INVALIDARG. The <b>IViewObjectEx::GetViewStatus</b> method allows the container to get back information about all drawing aspects in one quick call. Normally the set of supported drawing aspects should not change with time. However, if this was not the case, an object should notify its container using <a href="https://msdn.microsoft.com/9d5129aa-341c-4c69-8c0c-b7c3e62a57c1">IAdviseSinkEx::OnViewStatusChange</a>.

Which drawing aspects are supported is independent of whether the object is opaque, partially transparent, or totally transparent. In particular, a transparent object that does not support DVASPECT_TRANSPARENT should be drawn correctly during the back to front pass using DVASPECT_CONTENT. However, this is likely to result in more flicker.




## -see-also




<a href="https://msdn.microsoft.com/9d5129aa-341c-4c69-8c0c-b7c3e62a57c1">IAdviseSinkEx::OnViewStatusChange</a>



<a href="https://msdn.microsoft.com/4e677ec6-9c9e-4ee7-bb7f-1df6e590319b">IViewObjectEx</a>



<a href="https://msdn.microsoft.com/7b3118af-db29-4eb1-9b1b-38a8ebe42f19">VIEWSTATUS</a>
 

 

