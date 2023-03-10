---
UID: NF:msrdc.ISimilarityTraitsMapping.GetPageSize
title: ISimilarityTraitsMapping::GetPageSize (msrdc.h)
description: Returns the page size (disk block size) for a similarity traits table file.
helpviewer_keywords: ["GetPageSize","GetPageSize method [Remote Differential Compression]","GetPageSize method [Remote Differential Compression]","ISimilarityTraitsMapping interface","ISimilarityTraitsMapping interface [Remote Differential Compression]","GetPageSize method","ISimilarityTraitsMapping.GetPageSize","ISimilarityTraitsMapping::GetPageSize","fs.isimilaritytraitsmapping_getpagesize","msrdc/ISimilarityTraitsMapping::GetPageSize","rdc.isimilaritytraitsmapping_getpagesize"]
old-location: rdc\isimilaritytraitsmapping_getpagesize.htm
tech.root: rdc
ms.assetid: 8189d346-9e8e-40c0-8080-75c36326c917
ms.date: 12/05/2018
ms.keywords: GetPageSize, GetPageSize method [Remote Differential Compression], GetPageSize method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],GetPageSize method, ISimilarityTraitsMapping.GetPageSize, ISimilarityTraitsMapping::GetPageSize, fs.isimilaritytraitsmapping_getpagesize, msrdc/ISimilarityTraitsMapping::GetPageSize, rdc.isimilaritytraitsmapping_getpagesize
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsMapping::GetPageSize
 - msrdc/ISimilarityTraitsMapping::GetPageSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMapping.GetPageSize
---

# ISimilarityTraitsMapping::GetPageSize


## -description

Returns the page size (disk block size) for a similarity traits table file.

## -parameters

### -param pageSize [out]

Pointer to a location that receives the page size, in bytes. This page size must be at least 65536 bytes.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>