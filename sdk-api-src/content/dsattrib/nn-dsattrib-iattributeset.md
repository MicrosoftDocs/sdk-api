---
UID: NN:dsattrib.IAttributeSet
title: IAttributeSet
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAttributeSet interface sets key/value pairs on an object, where the key is a GUID and the value is any binary data.
old-location: mstv\iattributeset.htm
tech.root: mstv
ms.assetid: ce10ae94-5bd5-4f97-a341-8d5f894bda59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAttributeSet, IAttributeSet interface [Microsoft TV Technologies], IAttributeSet interface [Microsoft TV Technologies],described, IAttributeSetInterface, dsattrib/IAttributeSet, mstv.iattributeset
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAttributeSet interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAttributeSet</b> interface sets key/value pairs on an object, where the key is a <b>GUID</b> and the value is any binary data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttributeSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAttributeSet</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5f2dc759-5545-4b4a-a2fc-fca65c0856cd">SetAttrib</a>
</td>
<td align="left" width="63%">
Sets an attribute on the object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAttributeSet)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/561267ac-8720-4aba-b812-784ab1e42114">IAttributeGet Interface</a>
 

 

