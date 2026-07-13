---
UID: NF:tapi3ds.ITAllocatorProperties.SetAllocateBuffers
title: ITAllocatorProperties::SetAllocateBuffers (tapi3ds.h)
description: The ITAllocatorProperties::SetAllocateBuffers method (tapi3ds.h) determines whether the current allocator buffers must be set.
helpviewer_keywords: ["ITAllocatorProperties interface [TAPI 2.2]","SetAllocateBuffers method","ITAllocatorProperties.SetAllocateBuffers","ITAllocatorProperties::SetAllocateBuffers","SetAllocateBuffers","SetAllocateBuffers method [TAPI 2.2]","SetAllocateBuffers method [TAPI 2.2]","ITAllocatorProperties interface","_tapi3_itallocatorproperties_setallocatebuffers","tapi3.itallocatorproperties_setallocatebuffers","tapi3ds/ITAllocatorProperties::SetAllocateBuffers"]
old-location: tapi3\itallocatorproperties_setallocatebuffers.htm
tech.root: tapi3
ms.assetid: 5f4a25f8-1a5f-40ff-9a29-586d1c7c217c
ms.date: 08/10/2022
ms.keywords: ITAllocatorProperties interface [TAPI 2.2],SetAllocateBuffers method, ITAllocatorProperties.SetAllocateBuffers, ITAllocatorProperties::SetAllocateBuffers, SetAllocateBuffers, SetAllocateBuffers method [TAPI 2.2], SetAllocateBuffers method [TAPI 2.2],ITAllocatorProperties interface, _tapi3_itallocatorproperties_setallocatebuffers, tapi3.itallocatorproperties_setallocatebuffers, tapi3ds/ITAllocatorProperties::SetAllocateBuffers
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAllocatorProperties::SetAllocateBuffers
 - tapi3ds/ITAllocatorProperties::SetAllocateBuffers
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
 - ITAllocatorProperties.SetAllocateBuffers
---

# ITAllocatorProperties::SetAllocateBuffers


## -description

The 
<b>SetAllocateBuffers</b> method determines whether the current allocator buffers must be set. This property is <b>TRUE</b> by default. If set <b>FALSE</b>, the sample that the MST allocated doesn't have any buffers and they must be supplied before Update is called on the samples.

## -parameters

### -param bAllocBuffers [in]

Boolean indicator of whether allocator buffers must be set.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
