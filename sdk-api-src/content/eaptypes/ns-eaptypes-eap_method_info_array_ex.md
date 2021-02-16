---
UID: NS:eaptypes._EAP_METHOD_INFO_ARRAY_EX
title: EAP_METHOD_INFO_ARRAY_EX (eaptypes.h)
description: Contains information about all of the EAP methods installed on the client computer.
helpviewer_keywords: ["EAP_METHOD_INFO_ARRAY_EX","EAP_METHOD_INFO_ARRAY_EX structure [EAPHost]","PEAP_METHOD_INFO_ARRAY_EX","PEAP_METHOD_INFO_ARRAY_EX structure pointer [EAPHost]","eaphost.eap_method_info_array_ex","eaptypes/EAP_METHOD_INFO_ARRAY_EX","eaptypes/PEAP_METHOD_INFO_ARRAY_EX"]
old-location: eaphost\eap_method_info_array_ex.htm
tech.root: eaphost
ms.assetid: 3deb04da-3071-4ddd-a7cb-82a1c47c3677
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_INFO_ARRAY_EX, EAP_METHOD_INFO_ARRAY_EX structure [EAPHost], PEAP_METHOD_INFO_ARRAY_EX, PEAP_METHOD_INFO_ARRAY_EX structure pointer [EAPHost], eaphost.eap_method_info_array_ex, eaptypes/EAP_METHOD_INFO_ARRAY_EX, eaptypes/PEAP_METHOD_INFO_ARRAY_EX
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.typenames: EAP_METHOD_INFO_ARRAY_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_INFO_ARRAY_EX
 - eaptypes/_EAP_METHOD_INFO_ARRAY_EX
 - EAP_METHOD_INFO_ARRAY_EX
 - eaptypes/EAP_METHOD_INFO_ARRAY_EX
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
 - EAP_METHOD_INFO_ARRAY_EX
---

# EAP_METHOD_INFO_ARRAY_EX structure


## -description

The <b>EAP_METHOD_INFO_ARRAY_EX</b> structure contains information about all of the EAP methods installed on the client computer. After populating <b>EAP_METHOD_INFO_ARRAY_EX</b>, EAPHost passes this method information to the supplicant.

## -struct-fields

### -field dwNumberOfMethods

The number of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex">EAP_METHOD_INFO_EX</a> structures in <b>pEapMethods</b>.

### -field pEapMethods

Pointer to the address of the first element in an array of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex">EAP_METHOD_INFO_EX</a> structures. The total number of elements is specified in <b>dwNumberOfMethods</b>.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)



[EAP Method Properties](/windows/win32/eaphost/eap-method-properties)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info">EAP_METHOD_INFO</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array">EAP_METHOD_INFO_ARRAY</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex">EAP_METHOD_INFO_EX</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>