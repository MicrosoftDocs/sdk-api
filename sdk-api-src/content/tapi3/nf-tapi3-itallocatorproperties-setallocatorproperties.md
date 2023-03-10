---
UID: NF:tapi3.ITAllocatorProperties.SetAllocatorProperties
title: ITAllocatorProperties::SetAllocatorProperties (tapi3.h)
description: The ITAllocatorProperties::SetAllocatorProperties (tapi3.h) method must be called before connection and will force the MSP to use these values during filter negotiation.
helpviewer_keywords: ["ITAllocatorProperties interface [TAPI 2.2]","SetAllocatorProperties method","ITAllocatorProperties.SetAllocatorProperties","ITAllocatorProperties::SetAllocatorProperties","SetAllocatorProperties","SetAllocatorProperties method [TAPI 2.2]","SetAllocatorProperties method [TAPI 2.2]","ITAllocatorProperties interface","_tapi3_itallocatorproperties_setallocatorproperties","tapi3.itallocatorproperties_setallocatorproperties","tapi3ds/ITAllocatorProperties::SetAllocatorProperties"]
old-location: tapi3\itallocatorproperties_setallocatorproperties.htm
tech.root: tapi3
ms.assetid: 3ab13fac-2667-44ce-aa1a-72cd18d37b0a
ms.date: 08/09/2022
ms.keywords: ITAllocatorProperties interface [TAPI 2.2],SetAllocatorProperties method, ITAllocatorProperties.SetAllocatorProperties, ITAllocatorProperties::SetAllocatorProperties, SetAllocatorProperties, SetAllocatorProperties method [TAPI 2.2], SetAllocatorProperties method [TAPI 2.2],ITAllocatorProperties interface, _tapi3_itallocatorproperties_setallocatorproperties, tapi3.itallocatorproperties_setallocatorproperties, tapi3ds/ITAllocatorProperties::SetAllocatorProperties
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAllocatorProperties::SetAllocatorProperties
 - tapi3/ITAllocatorProperties::SetAllocatorProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAllocatorProperties.SetAllocatorProperties
---

# ITAllocatorProperties::SetAllocatorProperties


## -description

The 
<b>SetAllocatorProperties</b> method must be called before connection and will force the MSP to use these values during filter negotiation. If the connecting filter doesn't accept these values, the connection is not established.

## -parameters

### -param pAllocProperties [in]

Pointer to the allocator buffer.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

<b>This method should be used with extreme care.</b> The quality of the sound may suffer if the values entered for this method are not optimal for the MSP. Therefore, the application should know exactly the properties preferred by the MSP before calling this method. Under Windows 2000, properties entered during calls to this method are ignored if they are not optimal. Under Windows XP, these values are not ignored and the application must be more knowledgeable.

If the application is only concerned with setting consistent buffer sizes, the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-setbuffersize">ITAllocatorProperties::SetBufferSize</a> method should be used instead. This guarantees the application is provided with the specified buffer size.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
