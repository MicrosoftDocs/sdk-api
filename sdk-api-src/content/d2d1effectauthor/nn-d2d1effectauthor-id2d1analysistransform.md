---
UID: NN:d2d1effectauthor.ID2D1AnalysisTransform
title: ID2D1AnalysisTransform (d2d1effectauthor.h)
author: windows-sdk-content
description: Supplies data to an analysis effect.
old-location: direct2d\id2d1analysistransform.htm
tech.root: Direct2D
ms.assetid: 64CDA0A7-2790-436C-9EFC-3A74D09602B9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1AnalysisTransform, ID2D1AnalysisTransform interface [Direct2D], ID2D1AnalysisTransform interface [Direct2D],described, d2d1effectauthor/ID2D1AnalysisTransform, direct2d.id2d1analysistransform
ms.topic: interface
f1_keywords: 
 - "d2d1effectauthor/ID2D1AnalysisTransform"
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1AnalysisTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1AnalysisTransform interface


## -description


Supplies data to an analysis effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1AnalysisTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1AnalysisTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1AnalysisTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1analysistransform-processanalysisresults">ProcessAnalysisResults</a>
</td>
<td align="left" width="63%">
Supplies the analysis data to an analysis transform.

</td>
</tr>
</table> 


## -remarks



 This interface can be implemented by either an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform">ID2D1DrawTransform</a> or an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform">ID2D1ComputeTransform</a>.



