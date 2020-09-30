---
UID: NN:gpmgmt.IGPMGPOLinksCollection
title: IGPMGPOLinksCollection (gpmgmt.h)
description: The IGPMGPOLinksCollection interface contains methods that enable applications to access a collection of GPO links when using the Group Policy Management (GPMC) interfaces.
helpviewer_keywords: ["GPMGPOLinksCollection","IGPMGPOLinksCollection","IGPMGPOLinksCollection interface [GPMC]","IGPMGPOLinksCollection interface [GPMC]","described","_win32_igpmgpolinkscollection","gpmc.igpmgpolinkscollection","gpmgmt/IGPMGPOLinksCollection"]
old-location: gpmc\igpmgpolinkscollection.htm
tech.root: gpmc
ms.assetid: 37753a31-0ef8-4fb9-b542-a91ae47ed417
ms.date: 12/05/2018
ms.keywords: GPMGPOLinksCollection, IGPMGPOLinksCollection, IGPMGPOLinksCollection interface [GPMC], IGPMGPOLinksCollection interface [GPMC],described, _win32_igpmgpolinkscollection, gpmc.igpmgpolinkscollection, gpmgmt/IGPMGPOLinksCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMGPOLinksCollection
 - gpmgmt/IGPMGPOLinksCollection
dev_langs:
 - c++
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
---

# IGPMGPOLinksCollection interface


## -description

The 
<b>IGPMGPOLinksCollection</b> interface contains methods that enable applications to access a collection of GPO links when using the Group Policy Management (GPMC) interfaces.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMGPOLinksCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMGPOLinksCollection</b> also has these types of members:
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
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpolinkscollection-get__newenum">get__NewEnum</a>
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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolink">IGPMGPOLink</a>