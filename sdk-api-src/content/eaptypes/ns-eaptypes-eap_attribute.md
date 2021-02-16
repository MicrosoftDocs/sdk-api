---
UID: NS:eaptypes._EAP_ATTRIBUTE
title: EAP_ATTRIBUTE (eaptypes.h)
description: Contains an EAP attribute.
helpviewer_keywords: ["EAP_ATTRIBUTE","EAP_ATTRIBUTE structure [EAPHost]","EapAttribute","EapAttribute structure [EAPHost]","eaphost.eap_attribute","eaptypes/EAP_ATTRIBUTE","eaptypes/EapAttribute"]
old-location: eaphost\eap_attribute.htm
tech.root: eaphost
ms.assetid: a8fe754a-ce6f-45f4-9536-7ffda2183e9e
ms.date: 12/05/2018
ms.keywords: EAP_ATTRIBUTE, EAP_ATTRIBUTE structure [EAPHost], EapAttribute, EapAttribute structure [EAPHost], eaphost.eap_attribute, eaptypes/EAP_ATTRIBUTE, eaptypes/EapAttribute
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EAP_ATTRIBUTE, EapAttribute
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_ATTRIBUTE
 - eaptypes/_EAP_ATTRIBUTE
 - EAP_ATTRIBUTE
 - eaptypes/EAP_ATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_ATTRIBUTE
---

## -description

The <b>EAP_ATTRIBUTE</b> structure contains an EAP attribute.

## -struct-fields

### -field eaType

An <a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type">EAP_ATTRIBUTE_TYPE</a> enumeration value that describes the type of the EAP attribute value supplied in <b>pValue</b>.

### -field dwLength

The size, in bytes, of <b>pValue</b>.

### -field pValue

Pointer to a byte buffer that contains the data value of the attribute.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EAP_ATTRIBUTES</a>
