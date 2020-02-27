---
UID: NN:comsvcs.IEnumNames
title: IEnumNames (comsvcs.h)
description: Enumerates names.
old-location: cos\ienumnames.htm
tech.root: cossdk
ms.assetid: 9f70b554-3cdd-4a4b-b180-c6de6182a46a
ms.date: 12/05/2018
ms.keywords: IEnumNames, IEnumNames interface [COM+], IEnumNames interface [COM+],described, _cos_IEnumNames, comsvcs/IEnumNames, cos.ienumnames
f1_keywords:
- comsvcs/IEnumNames
dev_langs:
- c++
req.header: comsvcs.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IEnumNames
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNames interface


## -description


Enumerates names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNames</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNames</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-methods-vb">Methods</a></li>
</ul>

## -members

The <b>IEnumNames</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ienumnames-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ienumnames-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ienumnames-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ienumnames-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icontextproperties">IContextProperties</a>
 

 

