---
UID: NN:faxcomex.IFaxDeviceIds
title: IFaxDeviceIds (faxcomex.h)
description: The IFaxDeviceIds interface defines a configuration collection used by a fax client application to enumerate the ordered fax device IDs associated with a FaxOutboundRoutingGroup object.
helpviewer_keywords: ["IFaxDeviceIds","IFaxDeviceIds interface [Fax Service]","IFaxDeviceIds interface [Fax Service]","described","_mfax_faxdeviceids_cpp","fax._mfax_faxdeviceids_cpp","faxcomex/IFaxDeviceIds"]
old-location: fax\_mfax_faxdeviceids_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_606r_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds, IFaxDeviceIds interface [Fax Service], IFaxDeviceIds interface [Fax Service],described, _mfax_faxdeviceids_cpp, fax._mfax_faxdeviceids_cpp, faxcomex/IFaxDeviceIds
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDeviceIds
 - faxcomex/IFaxDeviceIds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDeviceIds
---

# IFaxDeviceIds interface


## -description

The <b>IFaxDeviceIds</b> interface defines a configuration collection used by a fax client application to enumerate the ordered fax device IDs associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroup">FaxOutboundRoutingGroup</a> object. The collection includes methods to add, remove, and change the order of devices. The order of the devices in the collection determines the relative order in which available fax devices send outgoing transmissions.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceIds</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDeviceIds</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDeviceIds</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-add-vb">Add</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-add-vb">IFaxDeviceIds::Add</a> method adds a fax device to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection, using the device's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceids-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceids-get__newenum">IFaxDeviceIds::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceids-get_item">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceids-get_item">IFaxDeviceIds::get_Item</a> method represents a device ID from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-remove-vb">Remove</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-remove-vb">IFaxDeviceIds::Remove</a> method removes an item from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-setorder-vb">SetOrder</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-setorder-vb">IFaxDeviceIds::SetOrder</a> method changes the order of a device in the ordered <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceIds</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-count-vb">IFaxDeviceIds::get_Count</a> property represents the number of objects in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection. This is the total number of device IDs associated with the fax server.

</td>
</tr>
</table>

## -remarks

A default implementation of <b>IFaxDeviceIds</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> object.