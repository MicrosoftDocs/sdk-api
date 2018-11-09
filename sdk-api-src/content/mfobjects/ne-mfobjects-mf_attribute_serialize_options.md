---
UID: NE:mfobjects.MF_ATTRIBUTE_SERIALIZE_OPTIONS
title: MF_ATTRIBUTE_SERIALIZE_OPTIONS
author: windows-sdk-content
description: Defines flags for serializing and deserializing attribute stores.
old-location: mf\mf_attribute_serialize_options.htm
tech.root: medfound
ms.assetid: e4b218d1-185c-483f-b697-19ce8b3a4058
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MF_ATTRIBUTE_SERIALIZE_OPTIONS, MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration [Media Foundation], MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF, e4b218d1-185c-483f-b697-19ce8b3a4058, mf.mf_attribute_serialize_options, mfobjects/MF_ATTRIBUTE_SERIALIZE_OPTIONS, mfobjects/MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - MF_ATTRIBUTE_SERIALIZE_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MF_ATTRIBUTE_SERIALIZE_OPTIONS enumeration


## -description



Defines flags for serializing and deserializing attribute stores.




## -enum-fields




### -field MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF

If this flag is set, <b>IUnknown</b> pointers in the attribute store are marshaled to and from the stream. If this flag is absent, <b>IUnknown</b> pointers in the attribute store are not marshaled or serialized.


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a">MFDeserializeAttributesFromStream</a>



<a href="https://msdn.microsoft.com/b8bc88e5-19ae-46b3-aa78-a00afee1f481">MFSerializeAttributesToStream</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

