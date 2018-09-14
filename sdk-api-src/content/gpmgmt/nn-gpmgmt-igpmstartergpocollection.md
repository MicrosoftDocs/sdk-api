---
UID: NN:gpmgmt.IGPMStarterGPOCollection
title: IGPMStarterGPOCollection
author: windows-sdk-content
description: The IGPMStarterGPOCollection interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmstartergpocollection.htm
tech.root: GPMC
ms.assetid: b650b1c6-0597-468a-afdc-a21d61f1a8a0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMStarterGPOCollection, IGPMStarterGPOCollection, IGPMStarterGPOCollection interface [GPMC], IGPMStarterGPOCollection interface [GPMC],described, gpmc.igpmstartergpocollection, gpmgmt/IGPMStarterGPOCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStarterGPOCollection
 - IGPMStarterGPOCollection.Count
 - IGPMStarterGPOCollection.get_Count
 - IGPMStarterGPOCollection.Item
 - IGPMStarterGPOCollection.get_Item
 - GPMStarterGPOCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPOCollection interface


## -description


The 
<b>IGPMStarterGPOCollection</b> interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces. You can obtain a <b>GPMStarterGPOCollection</b> object by calling the 
<a href="https://msdn.microsoft.com/19a8efae-0b85-49ba-bf7e-08ed700874c3">IGPMDomain2::SearchStarterGPOs</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMStarterGPOCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStarterGPOCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e0e6360-46a9-49ff-9eb9-0ea708258ebb">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Count</b>

</td>
<td align="left" width="63%">
Number of GPOs in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific Starter GPO from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMStarterGPO</a>
 

 

