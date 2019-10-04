---
UID: NN:gpmgmt.IGPMCSECollection
title: IGPMCSECollection (gpmgmt.h)
author: windows-sdk-content
description: The IGPMCSECollection interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmcsecollection.htm
tech.root: gpmc
ms.assetid: e32c1c39-b817-4db6-ad76-b2e66b54d79d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMCSECollection, IGPMCSECollection, IGPMCSECollection interface [GPMC], IGPMCSECollection interface [GPMC],described, _win32_igpmcsecollection, gpmc.igpmcsecollection, gpmgmt/IGPMCSECollection
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMCSECollection"
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
 - IGPMCSECollection
 - IGPMCSECollection.Count
 - IGPMCSECollection.get_Count
 - IGPMCSECollection.Item
 - IGPMCSECollection.get_Item
 - GPMCSECollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMCSECollection interface


## -description


The 
<b>IGPMCSECollection</b> interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces. To create a <b>GPMCSECollection</b> object, call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getclientsideextensions">IGPM::GetClientSideExtensions</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMCSECollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMCSECollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMCSECollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmcsecollection-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMCSECollection</b> interface has these properties.
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
Number of CSEs in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
Index for a specific CSE from the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmclientsideextension">IGPMClientSideExtension</a>
 

 

