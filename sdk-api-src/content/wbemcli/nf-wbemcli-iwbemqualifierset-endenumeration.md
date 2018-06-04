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

# IWbemQualifierSet::EndEnumeration


## -description


Call the 
<b>IWbemQualifierSet::EndEnumeration</b> method when you plan to terminate enumerations initiated with 
<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a> and 
<a href="https://msdn.microsoft.com/76afa293-1bd9-442b-bc9b-2247459bd49c">IWbemQualifierSet::Next</a>. This call is recommended, but not required. It immediately releases resources associated with the enumeration.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a>



<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/76afa293-1bd9-442b-bc9b-2247459bd49c">IWbemQualifierSet::Next</a>
 

 

