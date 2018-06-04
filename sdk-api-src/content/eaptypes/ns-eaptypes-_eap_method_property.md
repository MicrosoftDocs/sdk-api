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

# _EAP_METHOD_PROPERTY structure


## -description


An <b>EAP_METHOD_PROPERTY</b> structure  contains an EAP method property.


## -struct-fields




### -field eapMethodPropertyType

An <a href="https://msdn.microsoft.com/49a62be4-5a8c-4e44-bdd1-aba37e3e7029">EAP_METHOD_PROPERTY_TYPE</a> enumeration value that describes the type of the EAP method property.


### -field eapMethodPropertyValueType

An <a href="https://msdn.microsoft.com/17ef654a-d4a0-45ba-a49d-45add8e78b28">EAP_METHOD_PROPERTY_VALUE_TYPE</a> enumeration value that describes the data type of the value specified in <b>eapMethodPropertyValue</b>.


### -field eapMethodPropertyValue.switch_is

 


### -field eapMethodPropertyValue.switch_is.eapMethodPropertyValueType

 


### -field eapMethodPropertyValue

An <a href="https://msdn.microsoft.com/298b59d3-245f-4a29-b8a1-2265d65d30e6">EAP_METHOD_PROPERTY_VALUE</a> union that contains the method property value.


## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/1dfe2fb2-a4e5-4c14-8cde-083e45134f7b">EAP_METHOD_PROPERTY_ARRAY</a>



<a href="https://msdn.microsoft.com/b553c022-c9a2-4cf7-8c09-e629b49cd929">EapHostPeerGetMethodProperties</a>
 

 

