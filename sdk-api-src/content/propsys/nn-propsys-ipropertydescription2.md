---
UID: NN:propsys.IPropertyDescription2
title: IPropertyDescription2
author: windows-sdk-content
description: Exposes methods that enumerate and retrieve individual property description details.
old-location: properties\IPropertyDescription2.htm
tech.root: properties
ms.assetid: 46c009b0-caf7-469f-9973-36d100a5ef98
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IPropertyDescription2, IPropertyDescription2 interface [Windows Properties], IPropertyDescription2 interface [Windows Properties],described, properties.IPropertyDescription2, propsys/IPropertyDescription2, shell.IPropertyDescription2, shell_IPropertyDescription2
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescription2 interface


## -description


Exposes methods that enumerate and retrieve individual property description details.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescription2</b> interface inherits from <a href="shell.IPropertyDescription">IPropertyDescription</a>. <b>IPropertyDescription2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescription2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescription2_GetImageReferenceForValue">GetImageReferenceForValue</a>
</td>
<td align="left" width="63%">
Gets the image reference associated with a property value.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface, from which it inherits.

To obtain this interface, call <a href="shell.PSGetPropertyDescription">PSGetPropertyDescription</a>, <a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a>, or <a href="shell.IPropertyDescriptionList_GetAt">IPropertyDescriptionList::GetAt</a>.

Only one property description exists for each property in the system.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="shell.IPropertyDescription">IPropertyDescription</a> in the system; it is provided by the Shell.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

