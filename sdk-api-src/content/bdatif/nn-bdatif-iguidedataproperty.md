---
UID: NN:bdatif.IGuideDataProperty
title: IGuideDataProperty (bdatif.h)
author: windows-sdk-content
description: The IGuideDataProperty interface represents the name, value, and language of a property associated with a service, program or schedule entry object.
old-location: mstv\iguidedataproperty.htm
tech.root: mstv
ms.assetid: 1c614f2a-69e0-4100-b83e-740478654c17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGuideDataProperty, IGuideDataProperty interface [Microsoft TV Technologies], IGuideDataProperty interface [Microsoft TV Technologies],described, IGuideDataPropertyInterface, bdatif/IGuideDataProperty, mstv.iguidedataproperty
ms.topic: interface
f1_keywords: 
 - "bdatif/IGuideDataProperty"
req.header: bdatif.h
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
 - Bdatif.h
api_name:
 - IGuideDataProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGuideDataProperty interface


## -description



The <b>IGuideDataProperty</b> interface represents the name, value, and language of a property associated with a service, program or schedule entry object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGuideDataProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGuideDataProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGuideDataProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataproperty-get_language">get_Language</a>
</td>
<td align="left" width="63%">
Retrieves the language associated with the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataproperty-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataproperty-get_value">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the property.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideDataProperty)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

