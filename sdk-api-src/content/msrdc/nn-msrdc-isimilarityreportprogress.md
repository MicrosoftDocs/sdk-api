---
UID: NN:msrdc.ISimilarityReportProgress
title: ISimilarityReportProgress (msrdc.h)
description: Defines a method for RDC to report the current completion percentage of a similarity operation.
helpviewer_keywords: ["ISimilarityReportProgress","ISimilarityReportProgress interface [Remote Differential Compression]","ISimilarityReportProgress interface [Remote Differential Compression]","described","fs.isimilarityreportprogress","msrdc/ISimilarityReportProgress","rdc.isimilarityreportprogress"]
old-location: rdc\isimilarityreportprogress.htm
tech.root: rdc
ms.assetid: 813bda93-08d5-456c-9bde-ce6dd53fb8bf
ms.date: 12/05/2018
ms.keywords: ISimilarityReportProgress, ISimilarityReportProgress interface [Remote Differential Compression], ISimilarityReportProgress interface [Remote Differential Compression],described, fs.isimilarityreportprogress, msrdc/ISimilarityReportProgress, rdc.isimilarityreportprogress
f1_keywords:
- msrdc/ISimilarityReportProgress
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- MsRdc.dll
api_name:
- ISimilarityReportProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityReportProgress interface


## -description


Defines a method for RDC to report the current completion percentage of a similarity operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityReportProgress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityReportProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityReportProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityreportprogress-reportprogress">ReportProgress</a>
</td>
<td align="left" width="63%">
Reports the current completion percentage of a similarity operation in progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

