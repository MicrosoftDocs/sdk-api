---
UID: NN:gpmgmt.IGPMGPOLink
title: IGPMGPOLink (gpmgmt.h)
description: The IGPMGPOLink interface supports methods that allow you to remove a GPO link from the scope of management (SOM), and to set and retrieve various properties of GPO links, including enabling and enforcing links.
old-location: gpmc\igpmgpolink.htm
tech.root: gpmc
ms.assetid: 290a53fb-8be0-477d-837c-46251b30e245
ms.date: 12/05/2018
ms.keywords: GPMGPOLink, IGPMGPOLink, IGPMGPOLink interface [GPMC], IGPMGPOLink interface [GPMC],described, _win32_igpmgpolink, gpmc.igpmgpolink, gpmgmt/IGPMGPOLink
ms.topic: interface
f1_keywords:
- gpmgmt/IGPMGPOLink
dev_langs:
- c++
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
- IGPMGPOLink
- GPMGPOLink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMGPOLink interface


## -description


The 
<b>IGPMGPOLink</b> interface supports methods that allow you to remove a GPO link from the scope of management (SOM), and to set and retrieve various properties of GPO links, including enabling and enforcing links.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMGPOLink</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMGPOLink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMGPOLink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpolink-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the GPO link from the SOM.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMGPOLink</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">Enabled</a>


</td>
<td align="left" width="63%">
Value that specifies whether the GPO link is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">Enforced</a>


</td>
<td align="left" width="63%">
Value that specifies whether the GPO link is enforced. If this property is equal to <b>TRUE</b>, the GPO link is enforced and cannot be overridden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">GPODomain</a>


</td>
<td align="left" width="63%">
Domain in which the GPO resides. This is a full DNS name, for example, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">GPOID</a>


</td>
<td align="left" width="63%">
ID of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">SOM</a>


</td>
<td align="left" width="63%">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">GPMSOM</a> object to which the GPO link is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpolink-property-methods">SOMLinkOrder</a>


</td>
<td align="left" width="63%">
Position of the GPO link in relation to other GPO links for the SOM.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">IGPMGPOLinksCollection</a>
 

 

