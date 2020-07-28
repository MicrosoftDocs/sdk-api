---
UID: NN:faxcomex.IFaxDeviceProviders
title: IFaxDeviceProviders (faxcomex.h)
description: The IFaxDeviceProviders interface defines a configuration collection which contains the fax device providers on a connected fax server.
helpviewer_keywords: ["IFaxDeviceProviders","IFaxDeviceProviders interface [Fax Service]","IFaxDeviceProviders interface [Fax Service]","described","_mfax_faxdeviceproviders_cpp","fax._mfax_faxdeviceproviders_cpp","faxcomex/IFaxDeviceProviders"]
old-location: fax\_mfax_faxdeviceproviders_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7vxv_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceProviders, IFaxDeviceProviders interface [Fax Service], IFaxDeviceProviders interface [Fax Service],described, _mfax_faxdeviceproviders_cpp, fax._mfax_faxdeviceproviders_cpp, faxcomex/IFaxDeviceProviders
f1_keywords:
- faxcomex/IFaxDeviceProviders
dev_langs:
- c++
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
- IFaxDeviceProviders
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDeviceProviders interface


## -description


The <b>IFaxDeviceProviders</b> interface defines a configuration collection which contains the fax device providers on a connected fax server. This collection is used by a fax client application to retrieve information about the fax service providers (FSPs) registered with the fax service, represented by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceProviders</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDeviceProviders</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDeviceProviders</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceproviders-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceproviders-get__newenum">IFaxDeviceProviders::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders">FaxDeviceProviders</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceproviders-get_item">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceproviders-get_item">IFaxDeviceProviders::get_Item</a> property returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a> object from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders">FaxDeviceProviders</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceProviders</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders-count-vb">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The Count property represents the number of objects in the FaxDeviceProviders collection. This is the total number of fax device providers associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDeviceProviders</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders">FaxDeviceProviders</a> object.



