---
UID: NN:msrdc.ISimilarityTableDumpState
title: ISimilarityTableDumpState (msrdc.h)
author: windows-sdk-content
description: Provides a method for retrieving information from the similarity traits list that was returned by the ISimilarityTraitsTable::BeginDump method.
old-location: rdc\isimilaritytabledumpstate.htm
tech.root: rdc
ms.assetid: a56433b5-191f-49fe-83fb-7057e4c30bbd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISimilarityTableDumpState, ISimilarityTableDumpState interface [Remote Differential Compression], ISimilarityTableDumpState interface [Remote Differential Compression],described, fs.isimilaritytabledumpstate, msrdc/ISimilarityTableDumpState, rdc.isimilaritytabledumpstate
ms.topic: interface
f1_keywords: 
 - "msrdc/ISimilarityTableDumpState"
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
 - ISimilarityTableDumpState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityTableDumpState interface


## -description


Provides a method for retrieving information from the similarity traits list that was returned by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-begindump">ISimilarityTraitsTable::BeginDump</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTableDumpState</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityTableDumpState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityTableDumpState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytabledumpstate-getnextdata">GetNextData</a>
</td>
<td align="left" width="63%">
Retrieves one or more <a href="https://docs.microsoft.com/windows/win32/api/msrdc/ns-msrdc-similaritydumpdata">SimilarityDumpData</a> structures from the similarity traits list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

