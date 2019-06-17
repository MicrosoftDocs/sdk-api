---
UID: NS:eaptypes._EAP_METHOD_PROPERTY
title: EAP_METHOD_PROPERTY (eaptypes.h)
author: windows-sdk-content
description: Contains an EAP method property.
old-location: eaphost\eap_method_property.htm
tech.root: eaphost
ms.assetid: df8c9ba2-e1c5-4011-bdbe-1d04765d19cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY, EAP_METHOD_PROPERTY structure [EAPHost], PEAP_METHOD_PROPERTY, PEAP_METHOD_PROPERTY structure pointer [EAPHost], eaphost.eap_method_property, eaptypes/EAP_METHOD_PROPERTY, eaptypes/PEAP_METHOD_PROPERTY
ms.topic: struct
f1_keywords: ["eaptypes/EAP_METHOD_PROPERTY"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapTypes.h
api_name:
 - EAP_METHOD_PROPERTY
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_PROPERTY
req.redist: 
ms.custom: 19H1
---

# EAP_METHOD_PROPERTY structure


## -description


An <b>EAP_METHOD_PROPERTY</b> structure  contains an EAP method property.


## -struct-fields




### -field eapMethodPropertyType

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ne-eaptypes-_eap_method_property_type">EAP_METHOD_PROPERTY_TYPE</a> enumeration value that describes the type of the EAP method property.


### -field eapMethodPropertyValueType

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ne-eaptypes-_eap_method_property_value_type">EAP_METHOD_PROPERTY_VALUE_TYPE</a> enumeration value that describes the data type of the value specified in <b>eapMethodPropertyValue</b>.


### -field eapMethodPropertyValue.switch_is

 


### -field eapMethodPropertyValue.switch_is.eapMethodPropertyValueType

 


### -field eapMethodPropertyValue

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property_value">EAP_METHOD_PROPERTY_VALUE</a> union that contains the method property value.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-structures">EAPHost Supplicant Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property_array">EAP_METHOD_PROPERTY_ARRAY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethodproperties">EapHostPeerGetMethodProperties</a>
 

 

