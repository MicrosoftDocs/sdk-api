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

# IWbemClassObject::BeginEnumeration


## -description


The 
<b>IWbemClassObject::BeginEnumeration</b> method resets an enumeration back to the beginning of the enumeration. The caller must call this method prior to the first call to 
<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a> to enumerate all of the properties on an object. The order in which properties are enumerated is guaranteed to be invariant for a given instance of 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>.


## -parameters




### -param lEnumFlags [in]

Combination of flags described in Remarks.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



You can control the properties included in the enumeration by specifying a combination of the following flags. You can combine one flag from each group with any flag from any other group. However, flags from the same group are mutually exclusive.

GROUP 1



GROUP 2






## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/a9fa8567-7504-4d59-a874-1dc7b2620a0b">IWbemClassObject::EndEnumeration</a>



<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a>



<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">WMI System Properties</a>
 

 

