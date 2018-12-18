---
UID: NN:mswmdm.ISCPSecureQuery
title: ISCPSecureQuery
author: windows-sdk-content
description: The ISCPSecureQuery interface is queried by Windows Media Device Manager to determine ownership of secured content.
old-location: wmdm\iscpsecurequery.htm
tech.root: WMDM
ms.assetid: d5f96629-26a1-4e83-a6a8-2d60c463f407
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISCPSecureQuery, ISCPSecureQuery interface [windows Media Device Manager], ISCPSecureQuery interface [windows Media Device Manager],described, ISCPSecureQueryInterface, mswmdm/ISCPSecureQuery, wmdm.iscpsecurequery
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - ISCPSecureQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureQuery interface


## -description



The <b>ISCPSecureQuery</b> interface is queried by Windows Media Device Manager to determine ownership of secured content. Windows Media Device Manager passes information about the content to the secure content provider, which uses that information to determine whether it is responsible for the content. Windows Media Device Manager consults this interface whenever an application downloads content to a media device.

The <a href="https://msdn.microsoft.com/fe5ae201-355d-4402-8d57-a721aecfdbde">ISCPSecureQuery2</a> interface extends <b>ISCPSecureQuery</b> through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.

The secure content provider implements this interface and secure Windows Media Device Manager implementations call its methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISCPSecureQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e12d8b55-5600-4178-8b2b-8afe8ade6818">ExamineData</a>
</td>
<td align="left" width="63%">
Determines whether the secure content provider is responsible for the content by examining data that Windows Media Device Manager passes to this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4ed4da1-9378-4c35-8f03-b028e37c1707">GetDataDemands</a>
</td>
<td align="left" width="63%">
Reports what data the secure content provider needs to determine rights and responsibility for a specified piece of content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d9991f4-ce20-45c4-a408-d7a846b019ef">GetRights</a>
</td>
<td align="left" width="63%">
Retrieves rights information for a piece of content. Rights are file-specific.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbcc8999-d7e4-4b67-a5ba-dd850ff7a07a">MakeDecision</a>
</td>
<td align="left" width="63%">
Determines whether transferring the content to a specified device is allowed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe5ae201-355d-4402-8d57-a721aecfdbde">ISCPSecureQuery2 Interface</a>



<a href="https://msdn.microsoft.com/3d600ae9-5d5b-48f6-a162-e52f78beb983">ISCPSecureQuery3 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

