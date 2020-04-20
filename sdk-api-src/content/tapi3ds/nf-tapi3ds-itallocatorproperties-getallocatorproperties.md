---
UID: NF:tapi3ds.ITAllocatorProperties.GetAllocatorProperties
title: ITAllocatorProperties::GetAllocatorProperties (tapi3ds.h)
description: The GetAllocatorProperties method gets the current values for the allocator properties after connection and provides the negotiated values. This method is invalid before connection. The MST will accept any values suggested by the connected filters.helpviewer_keywords: ["GetAllocatorProperties","GetAllocatorProperties method [TAPI 2.2]","GetAllocatorProperties method [TAPI 2.2]","ITAllocatorProperties interface","ITAllocatorProperties interface [TAPI 2.2]","GetAllocatorProperties method","ITAllocatorProperties.GetAllocatorProperties","ITAllocatorProperties::GetAllocatorProperties","_tapi3_itallocatorproperties_getallocatorproperties","tapi3.itallocatorproperties_getallocatorproperties","tapi3ds/ITAllocatorProperties::GetAllocatorProperties"]
old-location: tapi3\itallocatorproperties_getallocatorproperties.htm
tech.root: Tapi
ms.assetid: 67360904-a632-43cf-9f67-50bbdbb62f48
ms.date: 12/05/2018
ms.keywords: GetAllocatorProperties, GetAllocatorProperties method [TAPI 2.2], GetAllocatorProperties method [TAPI 2.2],ITAllocatorProperties interface, ITAllocatorProperties interface [TAPI 2.2],GetAllocatorProperties method, ITAllocatorProperties.GetAllocatorProperties, ITAllocatorProperties::GetAllocatorProperties, _tapi3_itallocatorproperties_getallocatorproperties, tapi3.itallocatorproperties_getallocatorproperties, tapi3ds/ITAllocatorProperties::GetAllocatorProperties
f1_keywords:
- tapi3ds/ITAllocatorProperties.GetAllocatorProperties
dev_langs:
- c++
req.header: tapi3ds.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITAllocatorProperties.GetAllocatorProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAllocatorProperties::GetAllocatorProperties


## -description


The 
<b>GetAllocatorProperties</b> method gets the current values for the allocator properties after connection and provides the negotiated values. This method is invalid before connection. The MST will accept any values suggested by the connected filters.


## -parameters




### -param pAllocProperties [out]

Pointer to current allocator values.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
 

 

