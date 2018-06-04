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

# IWbemClassObject::EndEnumeration


## -description


The 
<b>IWbemClassObject::EndEnumeration</b> method terminates an enumeration sequence started with 
<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>. This call is not required, but it is recommended to developers because it releases resources associated with the enumeration. However, the resources are deallocated automatically when the next enumeration is started or the object is released.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a>
 

 

