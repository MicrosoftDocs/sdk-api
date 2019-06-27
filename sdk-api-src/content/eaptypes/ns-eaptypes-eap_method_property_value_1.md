---
UID: NS:eaptypes._EAP_METHOD_PROPERTY_VALUE
title: EAP_METHOD_PROPERTY_VALUE (eaptypes.h)
author: windows-sdk-content
description: Contains the value of an EAP method property.
old-location: eaphost\eap_method_property_value.htm
tech.root: eaphost
ms.assetid: 298b59d3-245f-4a29-b8a1-2265d65d30e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY_VALUE, EAP_METHOD_PROPERTY_VALUE union [EAPHost], eaphost.eap_method_property_value, eaptypes/EAP_METHOD_PROPERTY_VALUE
ms.topic: struct
f1_keywords: 
 - "eaptypes/EAP_METHOD_PROPERTY_VALUE"
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
 - EAP_METHOD_PROPERTY_VALUE
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_PROPERTY_VALUE
req.redist: 
ms.custom: 19H1
---

# EAP_METHOD_PROPERTY_VALUE structure


## -description


The <b>EAP_METHOD_PROPERTY_VALUE</b> union contains the value of an EAP method property.


## -struct-fields




### -field empvBool

case(<i>empvtBool</i>)

If  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property">eapMethodPropertyValueType</a> specifies a Boolean type (<i>empvtBool</i>), the data pointed to by this parameter is defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property_value_bool">EAP_METHOD_PROPERTY_VALUE_BOOL</a> structure.


### -field empvDword

case(<i>empvDword</i>)

If <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property">eapMethodPropertyValueType</a> specifies a DWORD type (empvtDword), the data pointed to by this parameter is defined by the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property_value_dword">EAP_METHOD_PROPERTY_VALUE_DWORD</a> structure.


### -field empvString

case(<i>empvString</i>)

If <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property">eapMethodPropertyValueType</a> specifies a BYTE *(empvtString), the data pointed to by this parameter is defined by the   <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property_value_string">EAP_METHOD_PROPERTY_VALUE_STRING</a> structure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-structures">EAPHost Supplicant Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_property">EAP_METHOD_PROPERTY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethodproperties">EapHostPeerGetMethodProperties</a>
 

 

