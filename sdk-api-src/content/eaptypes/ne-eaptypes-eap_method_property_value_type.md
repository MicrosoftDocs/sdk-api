---
UID: NE:eaptypes._EAP_METHOD_PROPERTY_VALUE_TYPE
title: EAP_METHOD_PROPERTY_VALUE_TYPE (eaptypes.h)
description: Defines the set of possible data types for an EAP method property value.
helpviewer_keywords: ["EAP_METHOD_PROPERTY_VALUE_TYPE","EAP_METHOD_PROPERTY_VALUE_TYPE enumeration [EAPHost]","eaphost.eap_method_property_value_type","eaptypes/EAP_METHOD_PROPERTY_VALUE_TYPE","eaptypes/empvtBool","eaptypes/empvtDword","eaptypes/empvtString","empvtBool","empvtDword","empvtString"]
old-location: eaphost\eap_method_property_value_type.htm
tech.root: eaphost
ms.assetid: 17ef654a-d4a0-45ba-a49d-45add8e78b28
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY_VALUE_TYPE, EAP_METHOD_PROPERTY_VALUE_TYPE enumeration [EAPHost], eaphost.eap_method_property_value_type, eaptypes/EAP_METHOD_PROPERTY_VALUE_TYPE, eaptypes/empvtBool, eaptypes/empvtDword, eaptypes/empvtString, empvtBool, empvtDword, empvtString
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
req.typenames: EAP_METHOD_PROPERTY_VALUE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_PROPERTY_VALUE_TYPE
 - eaptypes/_EAP_METHOD_PROPERTY_VALUE_TYPE
 - EAP_METHOD_PROPERTY_VALUE_TYPE
 - eaptypes/EAP_METHOD_PROPERTY_VALUE_TYPE
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
 - EAP_METHOD_PROPERTY_VALUE_TYPE
---

# EAP_METHOD_PROPERTY_VALUE_TYPE enumeration


## -description

The <b>EAP_METHOD_PROPERTY_VALUE_TYPE</b> enumeration defines the set of possible data types for an EAP method property value.

## -enum-fields

### -field empvtBool:0

The method property value is of type <b>BOOL</b>.

### -field empvtDword

The method property value is of type <b>DWORD</b>.

### -field empvtString

The method property value is a pointer to a value of type  <b>BYTE</b>.

### -field v1_enum

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property">EAP_METHOD_PROPERTY</a>



<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_method_property_type">EAP_METHOD_PROPERTY_TYPE</a>
