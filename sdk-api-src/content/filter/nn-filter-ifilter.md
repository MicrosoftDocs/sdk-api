---
UID: NN:filter.IFilter
title: IFilter (filter.h)
description: Scans documents for text and properties (also called attributes).
helpviewer_keywords: ["IFilter","IFilter interface [Indexing Service]","IFilter interface [Indexing Service]","described","_idxs_IFilter","filter/IFilter","indexsrv.ifilter"]
old-location: indexsrv\ifilter.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_9sfm.htm
ms.date: 12/05/2018
ms.keywords: IFilter, IFilter interface [Indexing Service], IFilter interface [Indexing Service],described, _idxs_IFilter, filter/IFilter, indexsrv.ifilter
req.header: filter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilter
 - filter/IFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Filter.h
api_name:
 - IFilter
---

# IFilter interface


## -description

Scans documents for text and properties (also called attributes). It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text. It also extracts chunks of values, which are properties of an entire document or of well-defined parts of a document. <b>IFilter</b> provides the foundation for building higher-level applications such as document indexers and application-independent viewers.

For introductory information about how the <b>IFilter</b> interface works with documents and document properties, see <a href="/previous-versions/windows/desktop/indexsrv/properties-of-documents">Properties of Documents</a>. For a synopsis and an example of how the <b>IFilter</b> interface processes a document, see <a href="/previous-versions/windows/desktop/indexsrv/property-filtering">Property Filtering</a> and <a href="/previous-versions/windows/desktop/indexsrv/property-indexing">Property Indexing</a>.

## -inheritance

The <b>IFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilter</b> also has these types of members:

## -remarks

<b>IFilter</b> components for Indexing Service run in the Local Security context and should be written to manage buffers and to stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.

Previously, data returned by **IFilter** was only indexed lexically. Starting with Windows 11, version 26100, data returned **IFilter** is also semantically indexed. For example, users searching for "pasta" might also get results for "lasagna". Also starting with Windows 11, version 26100, the [IPixelFilter](nn-filter-ipixelfilter.md) enables semantic indexing of images. 

## -see-also

[BindIFilterFromStorage](/windows/desktop/api/ntquery/nf-ntquery-bindifilterfromstorage)

[BindIFilterFromStream](/windows/desktop/api/ntquery/nf-ntquery-bindifilterfromstream)

[LoadIFilter](/windows/desktop/api/ntquery/nf-ntquery-loadifilter)

