---
UID: NN:propsys.IPropertyDescriptionRelatedPropertyInfo
title: IPropertyDescriptionRelatedPropertyInfo
author: windows-sdk-content
description: Provides a method that retrives an IPropertyDescription interface.
old-location: properties\IPropertyDescriptionRelatedPropertyInfo.htm
old-project: properties
ms.assetid: 1658542e-ca2f-4566-b40f-8647577f4481
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPropertyDescriptionRelatedPropertyInfo, IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties], IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties],described, properties.IPropertyDescriptionRelatedPropertyInfo, propsys/IPropertyDescriptionRelatedPropertyInfo, shell.IPropertyDescriptionRelatedPropertyInfo, shell_IPropertyDescriptionRelatedPropertyInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionRelatedPropertyInfo
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: ADAM
---

# IPropertyDescriptionRelatedPropertyInfo interface


## -description


Provides a method that retrives an <a href="shell.IPropertyDescription">IPropertyDescription</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionRelatedPropertyInfo</b> interface inherits from <a href="shell.IPropertyDescription">IPropertyDescription</a>. <b>IPropertyDescriptionRelatedPropertyInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescriptionRelatedPropertyInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionRelatedPropertyInfo_GetRelatedProperty">GetRelatedProperty</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="shell.IPropertyDescription">IPropertyDescription</a> object that represents the related property.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="shell.IPropertyDescriptionRelatedPropertyInfo">IPropertyDescriptionRelatedPropertyInfo</a> in the system; it is provided by the Shell. 

Only one property description exists for each property in the system.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

