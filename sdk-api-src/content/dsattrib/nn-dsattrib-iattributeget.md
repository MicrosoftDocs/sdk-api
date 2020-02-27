---
UID: NN:dsattrib.IAttributeGet
title: IAttributeGet (dsattrib.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAttributeGet interface gets key/value pairs from an object, where the key is a GUID and the value is any binary data.
old-location: mstv\iattributeget.htm
tech.root: mstv
ms.assetid: 561267ac-8720-4aba-b812-784ab1e42114
ms.date: 12/05/2018
ms.keywords: IAttributeGet, IAttributeGet interface [Microsoft TV Technologies], IAttributeGet interface [Microsoft TV Technologies],described, IAttributeGetInterface, dsattrib/IAttributeGet, mstv.iattributeget
f1_keywords:
- dsattrib/IAttributeGet
dev_langs:
- c++
req.header: dsattrib.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dsattrib.h
api_name:
- IAttributeGet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAttributeGet interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAttributeGet</b> interface gets key/value pairs from an object, where the key is a <b>GUID</b> and the value is any binary data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttributeGet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAttributeGet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAttributeGet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nf-dsattrib-iattributeget-getattrib">GetAttrib</a>
</td>
<td align="left" width="63%">
Returns an attribute value, specified by <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nf-dsattrib-iattributeget-getattribindexed">GetAttribIndexed</a>
</td>
<td align="left" width="63%">
Returns an attribute value, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nf-dsattrib-iattributeget-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of attributes on this object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAttributeGet)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nn-dsattrib-iattributeset">IAttributeSet Interface</a>
 

 

