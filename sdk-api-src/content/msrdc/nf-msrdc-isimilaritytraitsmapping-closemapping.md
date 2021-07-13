---
UID: NF:msrdc.ISimilarityTraitsMapping.CloseMapping
title: ISimilarityTraitsMapping::CloseMapping (msrdc.h)
description: Closes a file mapping object for a similarity traits table file.
helpviewer_keywords: ["CloseMapping","CloseMapping method [Remote Differential Compression]","CloseMapping method [Remote Differential Compression]","ISimilarityTraitsMapping interface","ISimilarityTraitsMapping interface [Remote Differential Compression]","CloseMapping method","ISimilarityTraitsMapping.CloseMapping","ISimilarityTraitsMapping::CloseMapping","fs.isimilaritytraitsmapping_closemapping","msrdc/ISimilarityTraitsMapping::CloseMapping","rdc.isimilaritytraitsmapping_closemapping"]
old-location: rdc\isimilaritytraitsmapping_closemapping.htm
tech.root: rdc
ms.assetid: 9ac20c6b-9fe5-4b59-a9ed-faef97fd76f2
ms.date: 12/05/2018
ms.keywords: CloseMapping, CloseMapping method [Remote Differential Compression], CloseMapping method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],CloseMapping method, ISimilarityTraitsMapping.CloseMapping, ISimilarityTraitsMapping::CloseMapping, fs.isimilaritytraitsmapping_closemapping, msrdc/ISimilarityTraitsMapping::CloseMapping, rdc.isimilaritytraitsmapping_closemapping
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
 - ISimilarityTraitsMapping::CloseMapping
 - msrdc/ISimilarityTraitsMapping::CloseMapping
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
 - ISimilarityTraitsMapping.CloseMapping
---

# ISimilarityTraitsMapping::CloseMapping


## -description

Closes a file mapping object for a similarity traits table file.



## -remarks

Note that there may still be valid views open on the file. No new views may be created after the mapping is closed, but existing views continue to work.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
