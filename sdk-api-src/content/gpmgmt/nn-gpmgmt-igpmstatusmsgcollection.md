---
UID: NN:gpmgmt.IGPMStatusMsgCollection
title: IGPMStatusMsgCollection (gpmgmt.h)
author: windows-sdk-content
description: The IGPMStatusMsgCollection interface contains methods that enable applications to access a collection of status messages when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmstatusmsgcollection.htm
tech.root: gpmc
ms.assetid: 774dd1b0-e5ea-4fef-b3bc-743870793db5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMStatusMsgCollection, IGPMStatusMsgCollection, IGPMStatusMsgCollection interface [GPMC], IGPMStatusMsgCollection interface [GPMC],described, _win32_igpmstatusmsgcollection, gpmc.igpmstatusmsgcollection, gpmgmt/IGPMStatusMsgCollection
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
 - IGPMStatusMsgCollection
 - IGPMStatusMsgCollection.Count
 - IGPMStatusMsgCollection.get_Count
 - IGPMStatusMsgCollection.Item
 - IGPMStatusMsgCollection.get_Item
 - GPMStatusMsgCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMStatusMsgCollection interface


## -description


The 
<b>IGPMStatusMsgCollection</b> interface contains methods that enable applications to access a collection of status messages when using the Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMsgCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStatusMsgCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstatusmsgcollection-get__newenum">get__NewEnum</a>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">IGPMStatusMessage</a>
 

 

