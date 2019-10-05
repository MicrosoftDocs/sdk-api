---
UID: NF:tapi3ds.ITAllocatorProperties.GetAllocateBuffers
title: ITAllocatorProperties::GetAllocateBuffers (tapi3ds.h)
author: windows-sdk-content
description: The GetAllocateBuffers method determines whether the current allocator buffers can be retrieved. If it returns FALSE, the sample that the MST allocated doesn't have any buffers and they must be supplied before Update is called on the samples.
old-location: tapi3\itallocatorproperties_getallocatebuffers.htm
tech.root: Tapi
ms.assetid: 74058181-ab74-4a2d-8395-c8a1a7f02820
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllocateBuffers, GetAllocateBuffers method [TAPI 2.2], GetAllocateBuffers method [TAPI 2.2],ITAllocatorProperties interface, ITAllocatorProperties interface [TAPI 2.2],GetAllocateBuffers method, ITAllocatorProperties.GetAllocateBuffers, ITAllocatorProperties::GetAllocateBuffers, _tapi3_itallocatorproperties_getallocatebuffers, tapi3.itallocatorproperties_getallocatebuffers, tapi3ds/ITAllocatorProperties::GetAllocateBuffers
ms.topic: method
f1_keywords: 
 - "tapi3ds/ITAllocatorProperties.GetAllocateBuffers"
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
 - ITAllocatorProperties.GetAllocateBuffers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
 

 

