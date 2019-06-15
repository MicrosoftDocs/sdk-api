---
UID: NF:tapi3ds.ITAllocatorProperties.SetAllocateBuffers
title: ITAllocatorProperties::SetAllocateBuffers (tapi3ds.h)
author: windows-sdk-content
description: The SetAllocateBuffers method determines whether the current allocator buffers must be set.
old-location: tapi3\itallocatorproperties_setallocatebuffers.htm
tech.root: Tapi
ms.assetid: 5f4a25f8-1a5f-40ff-9a29-586d1c7c217c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAllocatorProperties interface [TAPI 2.2],SetAllocateBuffers method, ITAllocatorProperties.SetAllocateBuffers, ITAllocatorProperties::SetAllocateBuffers, SetAllocateBuffers, SetAllocateBuffers method [TAPI 2.2], SetAllocateBuffers method [TAPI 2.2],ITAllocatorProperties interface, _tapi3_itallocatorproperties_setallocatebuffers, tapi3.itallocatorproperties_setallocatebuffers, tapi3ds/ITAllocatorProperties::SetAllocateBuffers
ms.topic: method
f1_keywords: ["tapi3ds/ITAllocatorProperties.SetAllocateBuffers"]
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
 - ITAllocatorProperties.SetAllocateBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itallocatorproperties">ITAllocatorProperties</a>
 

 

