---
UID: NF:tapi3.ITAllocatorProperties.GetAllocateBuffers
title: ITAllocatorProperties::GetAllocateBuffers (tapi3.h)
description: The ITAllocatorProperties::GetAllocateBuffers (tapi3.h) method determines whether the current allocator buffers can be retrieved.
helpviewer_keywords: ["GetAllocateBuffers","GetAllocateBuffers method [TAPI 2.2]","GetAllocateBuffers method [TAPI 2.2]","ITAllocatorProperties interface","ITAllocatorProperties interface [TAPI 2.2]","GetAllocateBuffers method","ITAllocatorProperties.GetAllocateBuffers","ITAllocatorProperties::GetAllocateBuffers","_tapi3_itallocatorproperties_getallocatebuffers","tapi3.itallocatorproperties_getallocatebuffers","tapi3ds/ITAllocatorProperties::GetAllocateBuffers"]
old-location: tapi3\itallocatorproperties_getallocatebuffers.htm
tech.root: tapi3
ms.assetid: 74058181-ab74-4a2d-8395-c8a1a7f02820
ms.date: 08/09/2022
ms.keywords: GetAllocateBuffers, GetAllocateBuffers method [TAPI 2.2], GetAllocateBuffers method [TAPI 2.2],ITAllocatorProperties interface, ITAllocatorProperties interface [TAPI 2.2],GetAllocateBuffers method, ITAllocatorProperties.GetAllocateBuffers, ITAllocatorProperties::GetAllocateBuffers, _tapi3_itallocatorproperties_getallocatebuffers, tapi3.itallocatorproperties_getallocatebuffers, tapi3ds/ITAllocatorProperties::GetAllocateBuffers
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
 - ITAllocatorProperties::GetAllocateBuffers
 - tapi3/ITAllocatorProperties::GetAllocateBuffers
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
 - ITAllocatorProperties.GetAllocateBuffers
---

# ITAllocatorProperties::GetAllocateBuffers


## -description

The 
<b>GetAllocateBuffers</b> method determines whether the current allocator buffers can be retrieved. If it returns <b>FALSE</b>, the sample that the MST allocated doesn't have any buffers and they must be supplied before <b>Update</b> is called on the samples.

## -parameters

### -param pbAllocBuffers [out]

Indicates whether allocator buffers have been set.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
