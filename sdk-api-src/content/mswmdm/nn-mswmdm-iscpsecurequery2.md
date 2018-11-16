---
UID: NN:mswmdm.ISCPSecureQuery2
title: ISCPSecureQuery2
author: windows-sdk-content
description: The ISCPSecureQuery2 interface extends ISCPSecureQuery through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.
old-location: wmdm\iscpsecurequery2.htm
tech.root: WMDM
ms.assetid: fe5ae201-355d-4402-8d57-a721aecfdbde
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISCPSecureQuery2, ISCPSecureQuery2 interface [windows Media Device Manager], ISCPSecureQuery2 interface [windows Media Device Manager],described, ISCPSecureQuery2Interface, mswmdm/ISCPSecureQuery2, wmdm.iscpsecurequery2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISCPSecureQuery2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureQuery2 interface


## -description



The <b>ISCPSecureQuery2</b> interface extends <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a> through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureQuery2</b> interface inherits from <a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery</a>. <b>ISCPSecureQuery2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureQuery2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3031585-7a56-49d9-ad4b-d2f9e687dd6b">MakeDecision2</a>
</td>
<td align="left" width="63%">
Determines whether the secure content provider is responsible for the content by examining data that Windows Media Device Manager passes to this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery Interface</a>



<a href="https://msdn.microsoft.com/3d600ae9-5d5b-48f6-a162-e52f78beb983">ISCPSecureQuery3 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

