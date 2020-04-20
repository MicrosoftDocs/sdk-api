---
UID: NS:eaptypes._EAP_METHOD_INFO_EX
title: EAP_METHOD_INFO_EX (eaptypes.h)
description: Contains information about an EAP method.helpviewer_keywords: ["EAP_METHOD_INFO_EX","EAP_METHOD_INFO_EX structure [EAPHost]","eaphost.eap_method_info_ex","eaptypes/EAP_METHOD_INFO_EX"]
old-location: eaphost\eap_method_info_ex.htm
tech.root: eaphost
ms.assetid: 2d25f418-2130-4f9c-b3f4-f639dfba020a
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_INFO_EX, EAP_METHOD_INFO_EX structure [EAPHost], eaphost.eap_method_info_ex, eaptypes/EAP_METHOD_INFO_EX
f1_keywords:
- eaptypes/EAP_METHOD_INFO_EX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- eaptypes.h
api_name:
- EAP_METHOD_INFO_EX
targetos: Windows
req.typenames: EAP_METHOD_INFO_EX
req.redist: 
ms.custom: 19H1
---

# EAP_METHOD_INFO_EX structure


## -description


 The <b>EAP_METHOD_INFO_EX</b> structure contains  information about an EAP method.


## -struct-fields




### -field eaptype

 


### -field pwszAuthorName

Pointer to a zero-terminated Unicode string that contains the name of the EAP method's author.


### -field pwszFriendlyName

Pointer to a zero-terminated Unicode string that contains the display name of the EAP method.


### -field eapProperties

Set of flags that describe specific properties of the EAP methods. For flag descriptions, see [EAP Method Properties](https://docs.microsoft.com/windows/win32/eaphost/eap-method-properties)a>.


### -field pInnerMethodInfoArray

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex">EAP_METHOD_INFO_ARRAY_EX</a> structure that contains information about all of the EAP methods installed on the client computer.


#### - eapType

An <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that identifies the EAP method.


## -see-also




[Common EAPHost API Structures](https://docs.microsoft.com/windows/win32/eaphost/common-eap-host-api-structures)a>



[EAP Method Properties](https://docs.microsoft.com/windows/win32/eaphost/eap-method-properties)a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info">EAP_METHOD_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array">EAP_METHOD_INFO_ARRAY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex">EAP_METHOD_INFO_ARRAY_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a>
 

 

