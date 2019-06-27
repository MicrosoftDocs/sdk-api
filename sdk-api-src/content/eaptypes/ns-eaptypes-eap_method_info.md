---
UID: NS:eaptypes._EAP_METHOD_INFO
title: EAP_METHOD_INFO (eaptypes.h)
author: windows-sdk-content
description: Contains information about an EAP method.
old-location: eaphost\eap_method_info.htm
tech.root: eaphost
ms.assetid: 89b5dcbd-afa9-40a8-ab04-2caee01ce0a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_INFO, EAP_METHOD_INFO structure [EAPHost], eaphost.eap_method_info, eaptypes/EAP_METHOD_INFO
ms.topic: struct
f1_keywords: 
 - "eaptypes/EAP_METHOD_INFO"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_METHOD_INFO
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_INFO
req.redist: 
ms.custom: 19H1
---

# EAP_METHOD_INFO structure


## -description


 The <b>EAP_METHOD_INFO</b> structure contains  information about an EAP method.


## -struct-fields




### -field eaptype

 


### -field pwszAuthorName

Pointer to a zero-terminated Unicode string that contains the name of the EAP method's author.


### -field pwszFriendlyName

Pointer to a zero-terminated Unicode string that contains the display name of the EAP method.


### -field eapProperties

Set of flags that describe specific properties of the EAP method. For flag descriptions, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-method-properties">EAP Method Properties</a>.


### -field pInnerMethodInfo

Pointer to an <b>EAP_METHOD_INFO</b> structure that contains information about the inner method.


#### - eapType


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_type">EAP_METHOD_TYPE</a> structure that identifies the EAP method.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/common-eap-host-api-structures">Common EAPHost API Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-method-properties">EAP Method Properties</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_info_array">EAP_METHOD_INFO_ARRAY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_info_array_ex">EAP_METHOD_INFO_ARRAY_EX</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_info_ex">EAP_METHOD_INFO_EX</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_type">EAP_METHOD_TYPE</a>
 

 

