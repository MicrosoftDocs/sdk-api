---
UID: NF:projectedfslib.PrjAllocateAlignedBuffer
title: PrjAllocateAlignedBuffer function (projectedfslib.h)
description: Allocates a buffer that meets the memory alignment requirements of the virtualization instance's storage device.
helpviewer_keywords: ["PrjAllocateAlignedBuffer","PrjAllocateAlignedBuffer function","ProjFS.prjallocatealignedbuffer","projectedfslib/PrjAllocateAlignedBuffer"]
old-location: projfs\prjallocatealignedbuffer.htm
tech.root: ProjFS
ms.assetid: 49B723CC-976D-44C6-91D9-0FB26CFD45CA
ms.date: 12/05/2018
ms.keywords: PrjAllocateAlignedBuffer, PrjAllocateAlignedBuffer function, ProjFS.prjallocatealignedbuffer, projectedfslib/PrjAllocateAlignedBuffer
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ProjectedFSLib.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PrjAllocateAlignedBuffer
 - projectedfslib/PrjAllocateAlignedBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PrjAllocateAlignedBuffer
---

# PrjAllocateAlignedBuffer function


## -description

Allocates a buffer that meets the memory alignment requirements of the virtualization instance's storage device.

## -parameters

### -param namespaceVirtualizationContext [in]

Opaque handle for the virtualization instance.

### -param size [in]

The size of the buffer required, in bytes.

## -returns

Returns NULL if the buffer could not be allocated.

## -remarks

Use [PrjFreeAlignedBuffer](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) to deallocate memory obtained by **PrjAllocateAlignedBuffer**.

