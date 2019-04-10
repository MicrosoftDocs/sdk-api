---
UID: NN:upnp.IUPnPServiceEnumProperty
title: IUPnPServiceEnumProperty (upnp.h)
author: windows-sdk-content
description: Use this interface to delay Service Control Protocol Description (SCPD) download and event subscription on the IUPnPService objects enumerated from the IUPnPServices object.
old-location: upnp\iupnpserviceenumproperty.htm
tech.root: upnp
ms.assetid: B63CCE08-548F-44D3-BAE3-84E4358F25AD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPServiceEnumProperty, IUPnPServiceEnumProperty interface [UPnP APIs], IUPnPServiceEnumProperty interface [UPnP APIs],described, upnp.iupnpserviceenumproperty, upnp/IUPnPServiceEnumProperty
ms.topic: interface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceEnumProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPServiceEnumProperty interface


## -description


Use this interface to delay Service Control Protocol Description (SCPD) download and event subscription on the <a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> objects enumerated from the <a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a> object.

This interface can be obtained through a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> off the <a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceEnumProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPServiceEnumProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceEnumProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B138A230-7523-4803-ACE8-4F636DD54D86">SetServiceEnumProperty</a>
</td>
<td align="left" width="63%">
Sets the flag that indicates  opt-in to the delayed SCPD download and event subscription. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>
 

 

