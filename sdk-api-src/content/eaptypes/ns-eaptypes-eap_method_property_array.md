---
UID: NS:eaptypes._EAP_METHOD_PROPERTY_ARRAY
title: EAP_METHOD_PROPERTY_ARRAY (eaptypes.h)
description: Contains an array of EAP method properties.
helpviewer_keywords: ["EAP_METHOD_PROPERTY_ARRAY","EAP_METHOD_PROPERTY_ARRAY structure [EAPHost]","PEAP_METHOD_PROPERTY_ARRAY","PEAP_METHOD_PROPERTY_ARRAY structure pointer [EAPHost]","eaphost.eap_method_property_array","eaptypes/EAP_METHOD_PROPERTY_ARRAY","eaptypes/PEAP_METHOD_PROPERTY_ARRAY"]
old-location: eaphost\eap_method_property_array.htm
tech.root: eaphost
ms.assetid: 1dfe2fb2-a4e5-4c14-8cde-083e45134f7b
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY_ARRAY, EAP_METHOD_PROPERTY_ARRAY structure [EAPHost], PEAP_METHOD_PROPERTY_ARRAY, PEAP_METHOD_PROPERTY_ARRAY structure pointer [EAPHost], eaphost.eap_method_property_array, eaptypes/EAP_METHOD_PROPERTY_ARRAY, eaptypes/PEAP_METHOD_PROPERTY_ARRAY
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
req.typenames: EAP_METHOD_PROPERTY_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_PROPERTY_ARRAY
 - eaptypes/_EAP_METHOD_PROPERTY_ARRAY
 - EAP_METHOD_PROPERTY_ARRAY
 - eaptypes/EAP_METHOD_PROPERTY_ARRAY
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
 - EAP_METHOD_PROPERTY_ARRAY
---

# EAP_METHOD_PROPERTY_ARRAY structure


## -description

The <b>EAP_METHOD_PROPERTY_ARRAY</b> structure contains an array of EAP method properties.

## -struct-fields

### -field dwNumberOfProperties

The number of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property">EAP_METHOD_PROPERTY</a> structures in <b>pMethodProperty</b>.

### -field pFields

### -field pFields.size_is

### -field pFields.size_is.dwNumberOfProperties

### -field pMethodProperty

Pointer to the address of the first element in an array of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property">EAP_METHOD_PROPERTY</a> structures. The total number of elements is specified in <b>dwNumberOfProperties</b>.

## -see-also

[EAPHost Supplicant Structures](/windows/win32/eaphost/eap-host-supplicant-structures)



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethodproperties">EapHostPeerGetMethodProperties</a>