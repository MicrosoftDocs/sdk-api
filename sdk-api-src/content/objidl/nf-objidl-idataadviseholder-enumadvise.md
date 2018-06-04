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

# IDataAdviseHolder::EnumAdvise


## -description


Returns an object that can be used to enumerate the current advisory connections.


## -parameters




### -param ppenumAdvise [out]

A pointer to an <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If the implementation returns <b>NULL</b> in *<i>ppenumAdvise</i>, there are no connections to advise sinks at this time.


## -returns



This method returns S_OK if the enumerator object is successfully instantiated or there are no connections.




## -remarks



This method must supply a pointer to an implementation of the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> interface. Its methods allow you to enumerate the data stored in an array of <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structures. You get a pointer to the OLE implementation of <a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a> through a call to <a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>, and then call <b>IDataAdviseHolder::EnumAdvise</b> to implement <a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">IDataObject::EnumDAdvise</a>.

Adding more advisory connections while the enumerator object is active has an undefined effect on the enumeration that results from this method.




## -see-also




<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">IDataObject::EnumDAdvise</a>



<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>
 

 

