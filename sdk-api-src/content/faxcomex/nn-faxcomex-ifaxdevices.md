---
UID: NN:faxcomex.IFaxDevices
title: IFaxDevices (faxcomex.h)
description: The IFaxDevices interface defines a collection used by a fax client application to manage fax devices, where each device is represented by a FaxDevice object.
helpviewer_keywords: ["IFaxDevices","IFaxDevices interface [Fax Service]","IFaxDevices interface [Fax Service]","described","_mfax_faxdevices_cpp","fax._mfax_faxdevices_cpp","faxcomex/IFaxDevices"]
old-location: fax\_mfax_faxdevices_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1eib_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevices, IFaxDevices interface [Fax Service], IFaxDevices interface [Fax Service],described, _mfax_faxdevices_cpp, fax._mfax_faxdevices_cpp, faxcomex/IFaxDevices
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
 - IFaxDevices
 - faxcomex/IFaxDevices
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
 - IFaxDevices
---

# IFaxDevices interface


## -description

The <b>IFaxDevices</b> interface defines a collection used by a fax client application to manage fax devices, where each device is represented by a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDevices</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get__newenum">IFaxDevices::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get_item">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get_item">IFaxDevices::get_Item</a> method returns a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection, using its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get_itembyid">get_ItemById</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get_itembyid">IFaxDevices::get_ItemById</a> method returns a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection, using its device ID.

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

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices-count-vb">IFaxDevices::get_Count</a> property represents the number of objects in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection. This is the total number of devices used by the fax server.

</td>
</tr>
</table>

## -remarks

A default implementation of <b>IFaxDevices</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> object.