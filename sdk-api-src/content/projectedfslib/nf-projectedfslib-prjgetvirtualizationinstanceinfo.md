---
UID: NF:projectedfslib.PrjGetVirtualizationInstanceInfo
title: PrjGetVirtualizationInstanceInfo function (projectedfslib.h)
description: Retrieves information about the virtualization instance.
helpviewer_keywords: ["PrjGetVirtualizationInstanceInfo","PrjGetVirtualizationInstanceInfo function","ProjFS.prjgetvirtualizationinstanceinfo","projectedfslib/PrjGetVirtualizationInstanceInfo"]
old-location: projfs\prjgetvirtualizationinstanceinfo.htm
tech.root: ProjFS
ms.assetid: 0C04D13F-862C-4E4C-9BC1-13E6FAC86E99
ms.date: 12/05/2018
ms.keywords: PrjGetVirtualizationInstanceInfo, PrjGetVirtualizationInstanceInfo function, ProjFS.prjgetvirtualizationinstanceinfo, projectedfslib/PrjGetVirtualizationInstanceInfo
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
 - PrjGetVirtualizationInstanceInfo
 - projectedfslib/PrjGetVirtualizationInstanceInfo
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
 - PrjGetVirtualizationInstanceInfo
---

# PrjGetVirtualizationInstanceInfo function


## -description

Retrieves information about the virtualization instance.

## -parameters

### -param namespaceVirtualizationContext [in]

An opaque handle for the virtualization instance.

### -param virtualizationInstanceInfo [out]

On input points to a buffer to fill with information about the virtualization instance. On successful return the buffer is filled in.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

ProjFS callback routines provide the virtualization instance handle in their callbackData parameters. A provider that manages multiple virtualization instances can use the InstanceID field of virtualizationInstanceInfo to identify which of its virtualization instances is receiving the callback. 


The provider can use the WriteAlignment member of virtualizationInstanceInfo to determine the correct values to use for the byteOffset and length parameters of <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a>.