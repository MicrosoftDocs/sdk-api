---
UID: NN:tapi3if.ITTAPI2
title: ITTAPI2 (tapi3if.h)
description: The ITTAPI2 interface derives from the ITTAPI interface. It adds additional methods on the TAPI object to support phone devices.
helpviewer_keywords: ["ITTAPI2","ITTAPI2 interface [TAPI 2.2]","ITTAPI2 interface [TAPI 2.2]","described","_tapi3_ittapi2","tapi3.ittapi2","tapi3if/ITTAPI2"]
old-location: tapi3\ittapi2.htm
tech.root: tapi3
ms.assetid: 8c67f31e-783e-4371-9f17-063f8ecfc069
ms.date: 12/05/2018
ms.keywords: ITTAPI2, ITTAPI2 interface [TAPI 2.2], ITTAPI2 interface [TAPI 2.2],described, _tapi3_ittapi2, tapi3.ittapi2, tapi3if/ITTAPI2
f1_keywords:
- tapi3if/ITTAPI2
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITTAPI2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPI2 interface


## -description


The 
<b>ITTAPI2</b> interface derives from the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a> interface. It adds additional methods on the TAPI object to support phone devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPI2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPI2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPI2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi2-createemptycollectionobject">CreateEmptyCollectionObject</a>
</td>
<td align="left" width="63%">
Creates an empty collection object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi2-enumeratephones">EnumeratePhones</a>
</td>
<td align="left" width="63%">
Enumerates the phone objects that are available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi2-get_phones">get_Phones</a>
</td>
<td align="left" width="63%">
Gets the collection of phone objects that are available.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>
 

 

