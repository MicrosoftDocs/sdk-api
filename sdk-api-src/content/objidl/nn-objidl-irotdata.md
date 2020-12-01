---
UID: NN:objidl.IROTData
title: IROTData (objidl.h)
description: Implemented by monikers to enable the running object table (ROT) to compare monikers against each other.
helpviewer_keywords: ["IROTData","IROTData interface [COM]","IROTData interface [COM]","described","_com_irotdata","com.irotdata","objidl/IROTData"]
old-location: com\irotdata.htm
tech.root: com
ms.assetid: 44ae8377-c375-4dc3-9f54-a5674e24763f
ms.date: 12/05/2018
ms.keywords: IROTData, IROTData interface [COM], IROTData interface [COM],described, _com_irotdata, com.irotdata, objidl/IROTData
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IROTData
 - objidl/IROTData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IROTData
---

# IROTData interface


## -description

Implemented by monikers to enable the running object table (ROT) to compare monikers against each other.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IROTData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IROTData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IROTData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-irotdata-getcomparisondata">GetComparisonData</a>
</td>
<td align="left" width="63%">
Retrieves data from a moniker that can be used to test the moniker for equality against another moniker.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>