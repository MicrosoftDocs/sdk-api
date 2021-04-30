---
UID: NS:eaptypes._EAP_METHOD_PROPERTY_VALUE_STRING
title: EAP_METHOD_PROPERTY_VALUE_STRING (eaptypes.h)
description: Contains the string value of an EAP method property.
helpviewer_keywords: ["EAP_METHOD_PROPERTY_VALUE_STRING","EAP_METHOD_PROPERTY_VALUE_STRING structure [EAPHost]","PEAP_METHOD_PROPERTY_VALUE_STRING","PEAP_METHOD_PROPERTY_VALUE_STRING structure pointer [EAPHost]","eaphost.eap_method_property_value_string","eaptypes/EAP_METHOD_PROPERTY_VALUE_STRING","eaptypes/PEAP_METHOD_PROPERTY_VALUE_STRING"]
old-location: eaphost\eap_method_property_value_string.htm
tech.root: eaphost
ms.assetid: afb2d8f3-c2b1-45b8-9ff3-814c8e4b1595
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY_VALUE_STRING, EAP_METHOD_PROPERTY_VALUE_STRING structure [EAPHost], PEAP_METHOD_PROPERTY_VALUE_STRING, PEAP_METHOD_PROPERTY_VALUE_STRING structure pointer [EAPHost], eaphost.eap_method_property_value_string, eaptypes/EAP_METHOD_PROPERTY_VALUE_STRING, eaptypes/PEAP_METHOD_PROPERTY_VALUE_STRING
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
targetos: Windows
req.typenames: EAP_METHOD_PROPERTY_VALUE_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_PROPERTY_VALUE_STRING
 - eaptypes/_EAP_METHOD_PROPERTY_VALUE_STRING
 - EAP_METHOD_PROPERTY_VALUE_STRING
 - eaptypes/EAP_METHOD_PROPERTY_VALUE_STRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapTypes.h
api_name:
 - EAP_METHOD_PROPERTY_VALUE_STRING
---

# EAP_METHOD_PROPERTY_VALUE_STRING structure


## -description

The <b>EAP_METHOD_PROPERTY_VALUE_STRING</b> structure contains the string value of an EAP method property.

## -struct-fields

### -field length

The size, in bytes, of <b>value</b>.

### -field value.size_is

### -field value.size_is.length

### -field value

Pointer to a byte buffer than contains the data value of an EAP method property.

## -see-also

[EAPHost Supplicant Structures](/windows/win32/eaphost/eap-host-supplicant-structures)



<a href="/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property_value">EAP_METHOD_PROPERTY_VALUE</a>



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethodproperties">EapHostPeerGetMethodProperties</a>