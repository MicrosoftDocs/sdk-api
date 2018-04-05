---
UID: NS:eaptypes._EAP_ATTRIBUTE
title: "_EAP_ATTRIBUTE"
author: windows-driver-content
description: Contains an EAP attribute.
old-location: eaphost\eap_attribute.htm
old-project: EAPHost
ms.assetid: a8fe754a-ce6f-45f4-9536-7ffda2183e9e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EAP_ATTRIBUTE, EAP_ATTRIBUTE structure [EAPHost], EapAttribute, EapAttribute structure [EAPHost], _EAP_ATTRIBUTE, eaphost.eap_attribute, eaptypes/EAP_ATTRIBUTE, eaptypes/EapAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: EAP_ATTRIBUTE, EapAttribute
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	eaptypes.h
api_name:
-	EAP_ATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_ATTRIBUTE structure


## -description


 The <b>EAP_ATTRIBUTE</b> structure contains an EAP attribute.


## -struct-fields




### -field eaType

 


### -field dwLength

The size, in bytes, of <b>pValue</b>.


### -field pValue

Pointer to a byte buffer that contains the data value of the attribute.


#### - eapType

An <a href="https://msdn.microsoft.com/1c6999f5-b455-4a8d-9967-dc27938e8737">EAP_ATTRIBUTE_TYPE</a> enumeration value that describes the type of the EAP attribute value supplied in <b>pValue</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a>
 

 

