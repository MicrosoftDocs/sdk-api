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

# IAdviseSink::OnViewChange


## -description


Notifies an object's registered advise sinks that its view has changed.


## -parameters




### -param dwAspect [in]

The aspect, or view, of the object. Contains a value taken from the <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> enumeration.


### -param lindex [in]

The portion of the view that has changed. Currently only -1 is valid.


## -returns



This method does not return a value.




## -remarks



Containers register to be notified when an object's view changes by calling <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>. After it is registered, the object will call the sink's <b>IAdviseSink::OnViewChange</b> method when appropriate. <b>OnViewChange</b> can be called when the object is in either the loaded or running state.

Even though <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> values are individual flag bits, <i>dwAspect</i> may represent only one value. That is, <i>dwAspect</i> cannot contain the result of an OR operation combining two or more <b>DVASPECT</b> values.

The <i>lindex</i> parameter represents the part of the aspect that is of interest. The value of <i>lindex</i> depends on the value of <i>dwAspect</i>. If <i>dwAspect</i> is either DVASPECT_THUMBNAIL or DVASPECT_ICON, <i>lindex</i> is ignored. If <i>dwAspect</i> is DVASPECT_CONTENT, <i>lindex</i> must be -1, which indicates that the entire view is of interest and is the only value that is currently valid.




## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>
 

 

