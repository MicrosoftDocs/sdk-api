---
UID: NF:dwrite.IDWriteTextLayout.GetClusterMetrics
title: IDWriteTextLayout::GetClusterMetrics (dwrite.h)
description: Retrieves logical properties and measurements of each glyph cluster.
helpviewer_keywords: ["GetClusterMetrics","GetClusterMetrics method [Direct Write]","GetClusterMetrics method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetClusterMetrics method","IDWriteTextLayout.GetClusterMetrics","IDWriteTextLayout::GetClusterMetrics","directwrite.IDWriteTextLayout_GetClusterMetrics","dwrite/IDWriteTextLayout::GetClusterMetrics"]
old-location: directwrite\IDWriteTextLayout_GetClusterMetrics.htm
tech.root: DirectWrite
ms.assetid: 3c8ca925-2149-48dc-a71a-4f6a40153c3e
ms.date: 12/05/2018
ms.keywords: GetClusterMetrics, GetClusterMetrics method [Direct Write], GetClusterMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetClusterMetrics method, IDWriteTextLayout.GetClusterMetrics, IDWriteTextLayout::GetClusterMetrics, directwrite.IDWriteTextLayout_GetClusterMetrics, dwrite/IDWriteTextLayout::GetClusterMetrics
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextLayout::GetClusterMetrics
 - dwrite/IDWriteTextLayout::GetClusterMetrics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout.GetClusterMetrics
---

# IDWriteTextLayout::GetClusterMetrics


## -description

 Retrieves logical properties and measurements of each glyph cluster.

## -parameters

### -param clusterMetrics [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics">DWRITE_CLUSTER_METRICS</a>*</b>

When this method returns, contains metrics, such as line-break or total advance width, for a glyph cluster.

### -param maxClusterCount

Type: <b>UINT32</b>

The maximum size of the <i>clusterMetrics</i> array.

### -param actualClusterCount [out]

Type: <b>UINT32*</b>

When this method returns, contains the actual size of the <i>clusterMetrics</i> array that is needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If <i>maxClusterCount</i> is not large enough, then E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), is
     returned and <i>actualClusterCount</i> is set to the number of clusters
     needed.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

