---
UID: NS:eaptypes._EAP_METHOD_INFO
title: EAP_METHOD_INFO (eaptypes.h)
description: Contains information about an EAP method. (EAP_METHOD_INFO)
helpviewer_keywords: ["EAP_METHOD_INFO","EAP_METHOD_INFO structure [EAPHost]","eaphost.eap_method_info","eaptypes/EAP_METHOD_INFO"]
old-location: eaphost\eap_method_info.htm
tech.root: eaphost
ms.assetid: 89b5dcbd-afa9-40a8-ab04-2caee01ce0a3
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_INFO, EAP_METHOD_INFO structure [EAPHost], eaphost.eap_method_info, eaptypes/EAP_METHOD_INFO
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
req.typenames: EAP_METHOD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_INFO
 - eaptypes/_EAP_METHOD_INFO
 - EAP_METHOD_INFO
 - eaptypes/EAP_METHOD_INFO
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
 - EAP_METHOD_INFO
---

## -description

The <b>EAP_METHOD_INFO</b> structure contains  information about an EAP method.

## -struct-fields

### -field eaptype

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that identifies the EAP method.

### -field pwszAuthorName

Pointer to a zero-terminated Unicode string that contains the name of the EAP method's author.

### -field pwszFriendlyName

Pointer to a zero-terminated Unicode string that contains the display name of the EAP method.

### -field eapProperties

Set of flags that describe specific properties of the EAP method. For flag descriptions, see [EAP Method Properties](/windows/win32/eaphost/eap-method-properties).

### -field pInnerMethodInfo

Pointer to an <b>EAP_METHOD_INFO</b> structure that contains information about the inner method.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)

[EAP Method Properties](/windows/win32/eaphost/eap-method-properties)

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array">EAP_METHOD_INFO_ARRAY</a>

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex">EAP_METHOD_INFO_ARRAY_EX</a>

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex">EAP_METHOD_INFO_EX</a>

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>
