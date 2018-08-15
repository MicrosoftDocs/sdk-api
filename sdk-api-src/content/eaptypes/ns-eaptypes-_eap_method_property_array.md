---
UID: NS:eaptypes._EAP_METHOD_PROPERTY_ARRAY
title: "_EAP_METHOD_PROPERTY_ARRAY"
author: windows-sdk-content
description: Contains an array of EAP method properties.
old-location: eaphost\eap_method_property_array.htm
old-project: eaphost
ms.assetid: 1dfe2fb2-a4e5-4c14-8cde-083e45134f7b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EAP_METHOD_PROPERTY_ARRAY, EAP_METHOD_PROPERTY_ARRAY structure [EAPHost], PEAP_METHOD_PROPERTY_ARRAY, PEAP_METHOD_PROPERTY_ARRAY structure pointer [EAPHost], _EAP_METHOD_PROPERTY_ARRAY, eaphost.eap_method_property_array, eaptypes/EAP_METHOD_PROPERTY_ARRAY, eaptypes/PEAP_METHOD_PROPERTY_ARRAY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EAP_METHOD_PROPERTY_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapTypes.h
api_name:
 - EAP_METHOD_PROPERTY_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_METHOD_PROPERTY_ARRAY structure


## -description


The <b>EAP_METHOD_PROPERTY_ARRAY</b> structure contains an array of EAP method properties.


## -struct-fields




### -field dwNumberOfProperties

The number of <a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">EAP_METHOD_PROPERTY</a> structures in <b>pMethodProperty</b>.


### -field pFields

 


### -field pFields.size_is

 


### -field pFields.size_is.dwNumberOfProperties

 


### -field pMethodProperty

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">EAP_METHOD_PROPERTY</a> structures. The total number of elements is specified in <b>dwNumberOfProperties</b>.


## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/b553c022-c9a2-4cf7-8c09-e629b49cd929">EapHostPeerGetMethodProperties</a>
 

 

