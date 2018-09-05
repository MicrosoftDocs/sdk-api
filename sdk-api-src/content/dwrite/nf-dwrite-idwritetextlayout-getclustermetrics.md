---
UID: NF:dwrite.IDWriteTextLayout.GetClusterMetrics
title: IDWriteTextLayout::GetClusterMetrics
author: windows-sdk-content
description: Retrieves logical properties and measurements of each glyph cluster.
old-location: directwrite\IDWriteTextLayout_GetClusterMetrics.htm
old-project: DirectWrite
ms.assetid: 3c8ca925-2149-48dc-a71a-4f6a40153c3e
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetClusterMetrics, GetClusterMetrics method [Direct Write], GetClusterMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetClusterMetrics method, IDWriteTextLayout.GetClusterMetrics, IDWriteTextLayout::GetClusterMetrics, directwrite.IDWriteTextLayout_GetClusterMetrics, dwrite/IDWriteTextLayout::GetClusterMetrics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout.GetClusterMetrics
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextLayout::GetClusterMetrics


## -description


 Retrieves logical properties and measurements of each glyph cluster.


## -parameters




### -param clusterMetrics [out, optional]

Type: <b><a href="https://msdn.microsoft.com/738b7f15-fcc5-4960-ac1f-ca530c448271">DWRITE_CLUSTER_METRICS</a>*</b>

When this method returns, contains metrics, such as line-break or total advance width, for a glyph cluster.


### -param maxClusterCount

Type: <b>UINT32</b>

The maximum size of the <i>clusterMetrics</i> array.


### -param actualClusterCount [out]

Type: <b>UINT32*</b>

When this method returns, contains the actual size of the <i>clusterMetrics</i> array that is needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If <i>maxClusterCount</i> is not large enough, then E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), is
     returned and <i>actualClusterCount</i> is set to the number of clusters
     needed.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

