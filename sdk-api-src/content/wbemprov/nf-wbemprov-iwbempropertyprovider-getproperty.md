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

# IWbemPropertyProvider::GetProperty


## -description


The 
<b>IWbemPropertyProvider::GetProperty</b> method is called by Windows Management to retrieve an individual property value.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param strLocale [in]

String indicating the desired locale in cases where the returned property value can be localized. If the property cannot be localized, the implementation can ignore this value.


### -param strClassMapping [in]

Literal copy of the string value for the <b>ClassContext</b> qualifier for the class. This points to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param strInstMapping [in]

Literal copy of the string value for the <b>InstanceContext</b> qualifier for the instance. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param strPropMapping [in]

Literal copy of the value of the <b>PropertyContext</b> qualifier for the property. This must point to a valid <b>BSTR</b>, which is treated as read-only, or <b>NULL</b> if the qualifier does not exist.


### -param pvValue [out]

Pointer to an uninitialized <b>VARIANT</b> that receives the value for the property. The implementation must call <b>VariantInit</b> and return the value. If an error occurs, the implementation is expected to ignore the pointer.


## -returns



This method must return <b>WBEM_S_NO_ERROR</b> if the call succeeds. If the call fails, the method must return <b>WBEM_S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a1c25c5c-e0f9-461d-96ba-7d6d00d24d33">Constructing Property Providers</a>



<a href="https://msdn.microsoft.com/8a7910ae-4258-4486-80ff-82b1081083cc">IWbemPropertyProvider</a>



<b>PutProperty</b>
 

 

