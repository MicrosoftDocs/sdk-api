---
UID: NN:gpmgmt.IGPMCSECollection
title: IGPMCSECollection
author: windows-sdk-content
description: The IGPMCSECollection interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmcsecollection.htm
old-project: GPMC
ms.assetid: e32c1c39-b817-4db6-ad76-b2e66b54d79d
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMCSECollection, IGPMCSECollection, IGPMCSECollection interface [GPMC], IGPMCSECollection interface [GPMC],described, _win32_igpmcsecollection, gpmc.igpmcsecollection, gpmgmt/IGPMCSECollection
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
 - IGPMCSECollection
 - IGPMCSECollection.Count
 - IGPMCSECollection.get_Count
 - IGPMCSECollection.Item
 - IGPMCSECollection.get_Item
 - GPMCSECollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMCSECollection interface


## -description


The 
<b>IGPMCSECollection</b> interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces. To create a <b>GPMCSECollection</b> object, call the 
<a href="https://msdn.microsoft.com/5bcf76f5-f216-4a33-9ac1-4cb98eb26db5">IGPM::GetClientSideExtensions</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMCSECollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a> interface. <b>IGPMCSECollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2c3b9e29-6c46-4ed1-9e60-2e71d8792020">get__NewEnum</a>
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




<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/b29f4d09-60c0-4c67-b295-05c7d9a05397">IGPMClientSideExtension</a>
 

 

