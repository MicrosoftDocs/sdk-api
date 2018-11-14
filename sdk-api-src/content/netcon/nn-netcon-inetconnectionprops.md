---
UID: NN:netcon.INetConnectionProps
title: INetConnectionProps
author: windows-sdk-content
description: Use the INetConnectionProps interface to retrieve the properties for a connection.
old-location: ics\inetconnectionprops.htm
tech.root: ICS
ms.assetid: 8152f75c-1c93-4c30-8a13-c47fd5dde4af
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetConnectionProps, INetConnectionProps interface [ICS/ICF], INetConnectionProps interface [ICS/ICF],described, _ics_inetconnectionprops, ics.inetconnectionprops, netcon/INetConnectionProps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetConnectionProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetConnectionProps interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

Use the 
<b>INetConnectionProps</b> interface to retrieve the properties for a connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetConnectionProps</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetConnectionProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetConnectionProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c24c5a6-d856-4c62-a98e-33e4fc216f83">get_DeviceName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device associated with the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df094bda-2e0f-4ff4-aff5-77d1703f8dee">get_Guid</a>
</td>
<td align="left" width="63%">
Retrieves the globally-unique identifier (GUID) for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cefaee7c-22ce-4171-8789-fe6befc7e313">get_MediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff91c38-51af-467b-baff-0d41a2ba14f7">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8d9506a-00a4-4202-aa1f-652a71cb5f0a">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the status of the connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bf2db553-f324-4f23-b96e-f8ae703aa3ea">INetSharingManager::get_NetConnectionProps</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

