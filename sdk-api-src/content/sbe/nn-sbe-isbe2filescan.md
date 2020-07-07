---
UID: NN:sbe.ISBE2FileScan
title: ISBE2FileScan (sbe.h)
description: Repairs a corrupted .WTV file.
helpviewer_keywords: ["ISBE2FileScan","ISBE2FileScan interface [Microsoft TV Technologies]","ISBE2FileScan interface [Microsoft TV Technologies]","described","mstv.isbe2filescan","sbe/ISBE2FileScan"]
old-location: mstv\isbe2filescan.htm
tech.root: mstv
ms.assetid: 95d59004-b182-42b8-b05e-920bfc5ea6a0
ms.date: 12/05/2018
ms.keywords: ISBE2FileScan, ISBE2FileScan interface [Microsoft TV Technologies], ISBE2FileScan interface [Microsoft TV Technologies],described, mstv.isbe2filescan, sbe/ISBE2FileScan
f1_keywords:
- sbe/ISBE2FileScan
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Sbe.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sbe.dll
api_name:
- ISBE2FileScan
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2FileScan interface


## -description


Repairs a corrupted .WTV file.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/filescan-object">FileScan</a> object implements this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2FileScan</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2FileScan</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2FileScan</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2filescan-repairfile">RepairFile</a>
</td>
<td align="left" width="63%">
Repairs a corrupted .WTV file.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2FileScan)</code>.



