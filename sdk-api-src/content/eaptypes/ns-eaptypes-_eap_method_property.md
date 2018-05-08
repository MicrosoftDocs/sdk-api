---
UID: NS:eaptypes._EAP_METHOD_PROPERTY
title: "_EAP_METHOD_PROPERTY"
author: windows-driver-content
description: Contains an EAP method property.
old-location: eaphost\eap_method_property.htm
old-project: EAPHost
ms.assetid: df8c9ba2-e1c5-4011-bdbe-1d04765d19cd
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EAP_METHOD_PROPERTY, EAP_METHOD_PROPERTY structure [EAPHost], PEAP_METHOD_PROPERTY, PEAP_METHOD_PROPERTY structure pointer [EAPHost], _EAP_METHOD_PROPERTY, eaphost.eap_method_property, eaptypes/EAP_METHOD_PROPERTY, eaptypes/PEAP_METHOD_PROPERTY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EAP_METHOD_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	EapTypes.h
api_name:
-	EAP_METHOD_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

