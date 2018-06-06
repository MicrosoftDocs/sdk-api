---
UID: NN:gpmgmt.IGPMStatusMsgCollection
title: IGPMStatusMsgCollection
author: windows-sdk-content
description: The IGPMStatusMsgCollection interface contains methods that enable applications to access a collection of status messages when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmstatusmsgcollection.htm
old-project: GPMC
ms.assetid: 774dd1b0-e5ea-4fef-b3bc-743870793db5
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMStatusMsgCollection, IGPMStatusMsgCollection, IGPMStatusMsgCollection interface [GPMC], IGPMStatusMsgCollection interface [GPMC],described, _win32_igpmstatusmsgcollection, gpmc.igpmstatusmsgcollection, gpmgmt/IGPMStatusMsgCollection
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStatusMsgCollection
 - IGPMStatusMsgCollection.Count
 - IGPMStatusMsgCollection.get_Count
 - IGPMStatusMsgCollection.Item
 - IGPMStatusMsgCollection.get_Item
 - GPMStatusMsgCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStatusMsgCollection interface


## -description


The 
<b>IGPMStatusMsgCollection</b> interface contains methods that enable applications to access a collection of status messages when using the Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMsgCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMStatusMsgCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStatusMsgCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2972c146-3e18-42e8-ab87-0b5530149eae">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMsgCollection</b> interface has these properties.
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
Number of messages in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific message from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">IGPMStatusMessage</a>
 

 

