---
UID: NF:msrdc.ISimilarity.CopyAndSwap
title: ISimilarity::CopyAndSwap (msrdc.h)
description: Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.
helpviewer_keywords: ["CopyAndSwap","CopyAndSwap method [Remote Differential Compression]","CopyAndSwap method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","CopyAndSwap method","ISimilarity.CopyAndSwap","ISimilarity::CopyAndSwap","fs.isimilarity_copyandswap","msrdc/ISimilarity::CopyAndSwap","rdc.isimilarity_copyandswap"]
old-location: rdc\isimilarity_copyandswap.htm
tech.root: rdc
ms.assetid: 3a31530e-da6d-4ac8-9fd4-d91419777ce5
ms.date: 12/05/2018
ms.keywords: CopyAndSwap, CopyAndSwap method [Remote Differential Compression], CopyAndSwap method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CopyAndSwap method, ISimilarity.CopyAndSwap, ISimilarity::CopyAndSwap, fs.isimilarity_copyandswap, msrdc/ISimilarity::CopyAndSwap, rdc.isimilarity_copyandswap
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
 - ISimilarity::CopyAndSwap
 - msrdc/ISimilarity::CopyAndSwap
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
 - ISimilarity.CopyAndSwap
---

# ISimilarity::CopyAndSwap


## -description

 Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.

After the <b>CopyAndSwap</b> method returns, the application continues to use the same <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a> object that it used before calling this method. However, the <b>ISimilarity</b> object is now associated with a different similarity file on disk.

## -parameters

### -param newSimilarityTables [in, optional]

An optional pointer to a temporary <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a> object that is used to create temporary copies of the tables. Before calling the <b>CopyAndSwap</b> method, the caller must call the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-createtable">CreateTable</a> method to create the temporary tables. On return, the caller must call the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-closetable">CloseTable</a> method to close the temporary tables.

### -param reportProgress [in, optional]

An optional pointer to an <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityreportprogress">ISimilarityReportProgress</a> object that will receive information on the progress of the copy-and-swap operation and allow the application to stop the copy operation. The caller must release this interface when it is no longer needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityreportprogress-reportprogress">ISimilarityReportProgress::ReportProgress</a>