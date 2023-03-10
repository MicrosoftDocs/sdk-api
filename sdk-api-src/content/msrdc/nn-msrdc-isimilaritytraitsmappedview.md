---
UID: NN:msrdc.ISimilarityTraitsMappedView
title: ISimilarityTraitsMappedView (msrdc.h)
description: Provides methods that an RDC application can implement for manipulating a mapped view of a similarity traits table file.
helpviewer_keywords: ["ISimilarityTraitsMappedView","ISimilarityTraitsMappedView interface [Remote Differential Compression]","ISimilarityTraitsMappedView interface [Remote Differential Compression]","described","fs.isimilaritytraitsmappedview","msrdc/ISimilarityTraitsMappedView","rdc.isimilaritytraitsmappedview"]
old-location: rdc\isimilaritytraitsmappedview.htm
tech.root: rdc
ms.assetid: 48d6d4a0-fbf1-476a-b30f-83176c51cb48
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsMappedView, ISimilarityTraitsMappedView interface [Remote Differential Compression], ISimilarityTraitsMappedView interface [Remote Differential Compression],described, fs.isimilaritytraitsmappedview, msrdc/ISimilarityTraitsMappedView, rdc.isimilaritytraitsmappedview
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
 - ISimilarityTraitsMappedView
 - msrdc/ISimilarityTraitsMappedView
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
 - ISimilarityTraitsMappedView
---

# ISimilarityTraitsMappedView interface


## -description

Provides methods that an RDC application can implement for manipulating a mapped view of a similarity traits table file.

This interface is used together with the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> interface to allow the application to provide the I/O services needed by the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a> and <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a> interfaces. The implementation model is based on memory mapped files, but the interface is rich enough to support other models as well, such as memory-only arrays or traditional file accesses.

A mapped view is used to map an area of the entire file into a contiguous block of memory. This mapping is valid until the view is changed or unmapped. A possible implementation would call the <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> function when the view is mapped (see the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitsmappedview-get">Get</a> method), and would then write the changes back to disk when the view is changed (see <b>Get</b>) or released (see the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitsmappedview-unmap">Unmap</a> method).

There can be multiple overlapping read-only mapped views of the same area of a file, and one or more read-only views can overlap a read/write view, but there can be only one read/write view of a given area of a file.

## -inheritance

The <b>ISimilarityTraitsMappedView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityTraitsMappedView</b> also has these types of members:

