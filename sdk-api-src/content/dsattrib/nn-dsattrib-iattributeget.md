---
UID: NN:dsattrib.IAttributeGet
title: IAttributeGet
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAttributeGet interface gets key/value pairs from an object, where the key is a GUID and the value is any binary data.
old-location: mstv\iattributeget.htm
old-project: mstv
ms.assetid: 561267ac-8720-4aba-b812-784ab1e42114
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAttributeGet, IAttributeGet interface [Microsoft TV Technologies], IAttributeGet interface [Microsoft TV Technologies],described, IAttributeGetInterface, dsattrib/IAttributeGet, mstv.iattributeget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DSA_NEWOBJ_DISPINFO, *LPDSA_NEWOBJ_DISPINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dsattrib.h
api_name:
-	IAttributeGet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAttributeGet interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAttributeGet</b> interface gets key/value pairs from an object, where the key is a <b>GUID</b> and the value is any binary data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttributeGet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAttributeGet</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/df1aad0c-7e71-4110-8e05-0af33dd04859">GetAttrib</a>
</td>
<td align="left" width="63%">
Returns an attribute value, specified by <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30fdd27f-99df-4ed6-b9ce-514b0e358854">GetAttribIndexed</a>
</td>
<td align="left" width="63%">
Returns an attribute value, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of attributes on this object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAttributeGet)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/ce10ae94-5bd5-4f97-a341-8d5f894bda59">IAttributeSet Interface</a>
 

 

