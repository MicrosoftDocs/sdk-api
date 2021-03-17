---
UID: NS:eaptypes._EAP_METHOD_INFO_ARRAY
title: EAP_METHOD_INFO_ARRAY (eaptypes.h)
description: Contains information on EAP methods installed on the client computer.
helpviewer_keywords: ["EAP_METHOD_INFO_ARRAY","EAP_METHOD_INFO_ARRAY structure [EAPHost]","PEAP_METHOD_INFO_ARRAY","PEAP_METHOD_INFO_ARRAY structure pointer [EAPHost]","eaphost.eap_method_info_array","eaptypes/EAP_METHOD_INFO_ARRAY","eaptypes/PEAP_METHOD_INFO_ARRAY"]
old-location: eaphost\eap_method_info_array.htm
tech.root: eaphost
ms.assetid: a3e2d5c0-eacd-46de-b092-6fd749870881
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_INFO_ARRAY, EAP_METHOD_INFO_ARRAY structure [EAPHost], PEAP_METHOD_INFO_ARRAY, PEAP_METHOD_INFO_ARRAY structure pointer [EAPHost], eaphost.eap_method_info_array, eaptypes/EAP_METHOD_INFO_ARRAY, eaptypes/PEAP_METHOD_INFO_ARRAY
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
req.typenames: EAP_METHOD_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_INFO_ARRAY
 - eaptypes/_EAP_METHOD_INFO_ARRAY
 - EAP_METHOD_INFO_ARRAY
 - eaptypes/EAP_METHOD_INFO_ARRAY
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
 - EAP_METHOD_INFO_ARRAY
---

# EAP_METHOD_INFO_ARRAY structure


## -description

The <b>EAP_METHOD_INFO_ARRAY</b> structure contains information on EAP methods installed on the client computer. After populating <b>EAP_METHOD_INFO_ARRAY</b>, EAPHost passes this method information to the supplicant.

## -struct-fields

### -field dwNumberOfMethods

The number of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info">EAP_METHOD_INFO</a> structures in <b>pEapMethods</b>.

### -field pEapMethods

Pointer to the address of the first element in an array of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info">EAP_METHOD_INFO</a> structures. The total number of elements is specified in <b>dwNumberOfMethods</b>.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)



[EAP Method Properties](/windows/win32/eaphost/eap-method-properties)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info">EAP_METHOD_INFO</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex">EAP_METHOD_INFO_ARRAY_EX</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex">EAP_METHOD_INFO_EX</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>