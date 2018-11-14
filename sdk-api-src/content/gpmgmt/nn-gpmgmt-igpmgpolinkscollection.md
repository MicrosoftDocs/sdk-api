---
UID: NN:gpmgmt.IGPMGPOLinksCollection
title: IGPMGPOLinksCollection
author: windows-sdk-content
description: The IGPMGPOLinksCollection interface contains methods that enable applications to access a collection of GPO links when using the Group Policy Management (GPMC) interfaces.
old-location: gpmc\igpmgpolinkscollection.htm
tech.root: GPMC
ms.assetid: 37753a31-0ef8-4fb9-b542-a91ae47ed417
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMGPOLinksCollection, IGPMGPOLinksCollection, IGPMGPOLinksCollection interface [GPMC], IGPMGPOLinksCollection interface [GPMC],described, _win32_igpmgpolinkscollection, gpmc.igpmgpolinkscollection, gpmgmt/IGPMGPOLinksCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGPMGPOLinksCollection
 - IGPMGPOLinksCollection.Count
 - IGPMGPOLinksCollection.get_Count
 - IGPMGPOLinksCollection.Item
 - IGPMGPOLinksCollection.get_Item
 - GPMGPOLinksCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPOLinksCollection interface


## -description


The 
<b>IGPMGPOLinksCollection</b> interface contains methods that enable applications to access a collection of GPO links when using the Group Policy Management (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMGPOLinksCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMGPOLinksCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMGPOLinksCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/953735c2-01d7-45e1-8417-6b18128de530">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMGPOLinksCollection</b> interface has these properties.
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
Number of GPO links in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific GPO link from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/290a53fb-8be0-477d-837c-46251b30e245">IGPMGPOLink</a>
 

 

