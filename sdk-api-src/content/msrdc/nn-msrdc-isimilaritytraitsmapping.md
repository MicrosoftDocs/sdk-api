---
UID: NN:msrdc.ISimilarityTraitsMapping
title: ISimilarityTraitsMapping (msrdc.h)
description: Provides methods that an RDC application can implement for creating and manipulating a file mapping object for a similarity traits table file.
helpviewer_keywords: ["ISimilarityTraitsMapping","ISimilarityTraitsMapping interface [Remote Differential Compression]","ISimilarityTraitsMapping interface [Remote Differential Compression]","described","fs.isimilaritytraitsmapping","msrdc/ISimilarityTraitsMapping","rdc.isimilaritytraitsmapping"]
old-location: rdc\isimilaritytraitsmapping.htm
tech.root: rdc
ms.assetid: 1ddc599b-5a9b-4807-9005-00793f9a6ed4
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsMapping, ISimilarityTraitsMapping interface [Remote Differential Compression], ISimilarityTraitsMapping interface [Remote Differential Compression],described, fs.isimilaritytraitsmapping, msrdc/ISimilarityTraitsMapping, rdc.isimilaritytraitsmapping
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
 - ISimilarityTraitsMapping
 - msrdc/ISimilarityTraitsMapping
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
 - ISimilarityTraitsMapping
---

# ISimilarityTraitsMapping interface


## -description

Provides methods that an RDC application can implement for creating and manipulating a file mapping object for  a similarity traits table file.

This interface is used together with the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmappedview">ISimilarityTraitsMappedView</a> interface to allow the application to provide the I/O services needed by the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a> and <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a> interfaces. The implementation model is based on memory mapped files, but the interface is rich enough to support other models as well, such as memory-only arrays or traditional file accesses.

This interface is used to represent the file on which multiple read-only or read/write views can be created. There can be multiple overlapping read-only mapped views of the same area of a file, and one or more read-only views can overlap a read/write view, but there can be only one read/write view of a given area of a file.

## -inheritance

The <b>ISimilarityTraitsMapping</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityTraitsMapping</b> also has these types of members:

