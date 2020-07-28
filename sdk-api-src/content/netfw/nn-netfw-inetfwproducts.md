---
UID: NN:netfw.INetFwProducts
title: INetFwProducts (netfw.h)
description: To access the methods and properties for registering third-party firewall products with Windows Firewall and for enumerating registered products.
helpviewer_keywords: ["INetFwProducts","INetFwProducts interface [ICS/ICF]","INetFwProducts interface [ICS/ICF]","described","ics.inetfwproducts","netfw/INetFwProducts"]
old-location: ics\inetfwproducts.htm
tech.root: ics
ms.assetid: 66608887-02df-4caf-91d0-e5091849ff32
ms.date: 12/05/2018
ms.keywords: INetFwProducts, INetFwProducts interface [ICS/ICF], INetFwProducts interface [ICS/ICF],described, ics.inetfwproducts, netfw/INetFwProducts
f1_keywords:
- netfw/INetFwProducts
dev_langs:
- c++
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FirewallAPI.dll
api_name:
- INetFwProducts
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwProducts interface


## -description


The <b>INetFwProducts</b> interface allows an application or service to access the methods and properties for registering third-party firewall  products with Windows Firewall and for enumerating registered products.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwProducts</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwProducts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwProducts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwproducts-item">Item</a>
</td>
<td align="left" width="63%">
Gets a product with a specified index in the product collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwproducts-register">Register</a>
</td>
<td align="left" width="63%">
Registers a third-party firewall product.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwProducts</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwproducts-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns an object supporting <a href="https://msdn.microsoft.com/library/ms221053.aspx">IEnumVariant</a> to enumerate the registered firewall products. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwproducts-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Accesses the count of registered third-party firewall products

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

