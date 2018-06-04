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

# IWbemClassObject::GetPropertyOrigin


## -description


The 
<b>IWbemClassObject::GetPropertyOrigin</b> method retrieves the name of the class in which a particular property was introduced. For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes. If the object does not inherit from a parent class, as in the case of a base class, for example, then the current class name is returned.


## -parameters




### -param wszName [in]

Property name for which the owning class name is desired. This must point to a valid <b>LPCWSTR</b>, which is treated as read-only.


### -param pstrClassName [out]

Pointer to the address of a new <b>BSTR</b> that receives the parent class name. To prevent memory leaks in the client process, the caller must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when the name is no longer required. This parameter must not point to a valid string before the method is called because this is an output parameter, and this pointer is not deallocated after the call is complete.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/05431e05-440e-4241-bde9-0dbd32039921">IWbemClassObject::InheritsFrom</a>
 

 

