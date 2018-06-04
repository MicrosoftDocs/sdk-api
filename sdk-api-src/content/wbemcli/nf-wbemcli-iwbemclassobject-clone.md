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

# IWbemClassObject::Clone


## -description


The 
<b>IWbemClassObject::Clone</b> method returns a new object that is a complete clone of the current object. The new object has a COM reference count of 1.


## -parameters




### -param ppCopy [out]

This parameter cannot be <b>NULL</b>. It receives the copy of the current object. You must call <b>IWbemClassObject::Release </b>on this object when it is no longer required.

A new object is not returned on error.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Use this method to duplicate a class definition, or to duplicate an instance. This can be useful when the original copy of the object is required for backup purposes while a new copy is modified. Likewise, use this method to create many new instances from a single source instance. For example, use 
<a href="https://msdn.microsoft.com/3f244c1b-60ed-41ff-8464-5ac66737a5da">IWbemClassObject::SpawnInstance</a> to create a single starting instance, and use 
<b>IWbemClassObject::Clone</b> to produce 100 copies of the instance quickly. Each object can be modified subsequently to take on its particular values.

It is not possible to use this method to convert a class definition into an instance, or convert an instance into a class definition.



