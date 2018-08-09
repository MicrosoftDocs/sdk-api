---
UID: NS:raseapif._RAS_AUTH_ATTRIBUTE
title: "_RAS_AUTH_ATTRIBUTE"
author: windows-sdk-content
description: The RAS_AUTH_ATTRIBUTE structure is used to pass authentication attributes, of type RAS_AUTH_ATTRIBUTE_TYPE, during an EAP session.
old-location: eap\ras_auth_attribute.htm
old-project: eap
ms.assetid: 36659154-de2b-4a94-b25e-b731a4ef9d99
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PRAS_AUTH_ATTRIBUTE, PRAS_AUTH_ATTRIBUTE, PRAS_AUTH_ATTRIBUTE structure pointer [EAP], RAS_AUTH_ATTRIBUTE, RAS_AUTH_ATTRIBUTE structure [EAP], _RAS_AUTH_ATTRIBUTE, _eap_ras_auth_attribute, eap.ras_auth_attribute, raseapif/PRAS_AUTH_ATTRIBUTE, raseapif/RAS_AUTH_ATTRIBUTE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RAS_AUTH_ATTRIBUTE, *PRAS_AUTH_ATTRIBUTE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - RAS_AUTH_ATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _RAS_AUTH_ATTRIBUTE structure


## -description


The 
<b>RAS_AUTH_ATTRIBUTE</b> structure is used to pass authentication attributes, of type 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>, during an EAP session.


## -struct-fields




### -field raaType

Specifies the type of attribute, as defined in the 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a> enumerated type.


### -field dwLength

Specifies the length in bytes of the value of this attribute. If the <b>Value</b> member is a pointer, <b>dwLength</b> specifies the length of the buffer pointed to. If the <b>Value</b> member is the value itself, <b>dwLength</b> specifies how much of the length of the <b>Value</b> member is taken up by the value.


### -field Value

Specifies the value of the attribute. Although this member is of the <b>PVOID</b> type, this member sometimes contains the value of the attribute rather than pointing to the value. The only way to know whether to interpret the <b>Value</b> member as a pointer to the value or the value itself, is to check the <b>raaType</b> member. See the reference page for 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a> for information about how the <b>Value</b> member should be interpreted for different types.


## -remarks



Often an array of these structures is used to store or obtain a set of attributes for a given user. Since the number of attributes for a session is unknown, the array must be dynamic. The array is terminated by a structure with an <b>raaType</b> member that has a value of <b>raatMinimum</b>.




## -see-also




<a href="https://msdn.microsoft.com/f2f1cf75-18d4-4764-a747-24662f166eb7">EAP Structures</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>
 

 

