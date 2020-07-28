---
UID: NN:dsattrib.IAttributeSet
title: IAttributeSet (dsattrib.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAttributeSet interface sets key/value pairs on an object, where the key is a GUID and the value is any binary data.
helpviewer_keywords: ["IAttributeSet","IAttributeSet interface [Microsoft TV Technologies]","IAttributeSet interface [Microsoft TV Technologies]","described","IAttributeSetInterface","dsattrib/IAttributeSet","mstv.iattributeset"]
old-location: mstv\iattributeset.htm
tech.root: mstv
ms.assetid: ce10ae94-5bd5-4f97-a341-8d5f894bda59
ms.date: 12/05/2018
ms.keywords: IAttributeSet, IAttributeSet interface [Microsoft TV Technologies], IAttributeSet interface [Microsoft TV Technologies],described, IAttributeSetInterface, dsattrib/IAttributeSet, mstv.iattributeset
f1_keywords:
- dsattrib/IAttributeSet
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
- IAttributeSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAttributeSet interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAttributeSet</b> interface sets key/value pairs on an object, where the key is a <b>GUID</b> and the value is any binary data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttributeSet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAttributeSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAttributeSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nf-dsattrib-iattributeset-setattrib">SetAttrib</a>
</td>
<td align="left" width="63%">
Sets an attribute on the object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAttributeSet)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nn-dsattrib-iattributeget">IAttributeGet Interface</a>
 

 

