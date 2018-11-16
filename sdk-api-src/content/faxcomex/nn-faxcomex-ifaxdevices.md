---
UID: NN:faxcomex.IFaxDevices
title: IFaxDevices
author: windows-sdk-content
description: The IFaxDevices interface defines a collection used by a fax client application to manage fax devices, where each device is represented by a FaxDevice object.
old-location: fax\_mfax_faxdevices_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1eib_cpp.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDevices, IFaxDevices interface [Fax Service], IFaxDevices interface [Fax Service],described, _mfax_faxdevices_cpp, fax._mfax_faxdevices_cpp, faxcomex/IFaxDevices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevices interface


## -description


The <b>IFaxDevices</b> interface defines a collection used by a fax client application to manage fax devices, where each device is represented by a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevices</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71475398-b724-4eaf-8776-b6059c449b88">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/71475398-b724-4eaf-8776-b6059c449b88">IFaxDevices::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca43bcd9-bb8d-44b9-b707-b088a0f466ab">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ca43bcd9-bb8d-44b9-b707-b088a0f466ab">IFaxDevices::get_Item</a> method returns a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection, using its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74863134-1ab8-49fc-ad59-f147ca8bdb45">get_ItemById</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/74863134-1ab8-49fc-ad59-f147ca8bdb45">IFaxDevices::get_ItemById</a> method returns a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection, using its device ID.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevices</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/44a0bbbb-7f5f-41de-9331-e473c155faaf">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/44a0bbbb-7f5f-41de-9331-e473c155faaf">IFaxDevices::get_Count</a> property represents the number of objects in the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection. This is the total number of devices used by the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDevices</b> is provided as the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> object.



