---
UID: NN:netcon.INetSharingPortMapping
title: INetSharingPortMapping
author: windows-sdk-content
description: The INetSharingPortMapping interface provides methods for managing a particular port mapping.
old-location: ics\inetsharingportmapping.htm
tech.root: ICS
ms.assetid: 236608c3-061e-4db0-96df-25d263b6463b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetSharingPortMapping, INetSharingPortMapping interface [ICS/ICF], INetSharingPortMapping interface [ICS/ICF],described, _ics_inetsharingportmapping, ics.inetsharingportmapping, netcon/INetSharingPortMapping
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
 - INetSharingPortMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingPortMapping interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingPortMapping</b> interface provides methods for managing a particular port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMapping</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetSharingPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9582110-a717-41a4-8ddd-26ef703b8356">Delete</a>
</td>
<td align="left" width="63%">
Deletes the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/110d9c9b-189c-4529-b960-2722d9037c7c">Disable</a>
</td>
<td align="left" width="63%">
Disables the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55a639f3-9180-4d02-9d10-659a398fa32f">Enable</a>
</td>
<td align="left" width="63%">
Enables the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cfc27a4-fe43-4e47-b857-7c80e8ee0dd5">get_Properties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for the port mapping.

</td>
</tr>
</table> 


## -remarks



Use the 
<a href="https://msdn.microsoft.com/0d9e1520-6018-425c-a2f9-c408fa3025cf">INetSharingConfiguration::AddPortMapping</a> and 
<a href="https://msdn.microsoft.com/f5465acc-2b36-47d1-b48f-b36df3a8efb3">INetSharingConfiguration::EnumPortMappings</a> methods to obtain 
<b>INetSharingPortMapping</b> interfaces.




## -see-also




<a href="https://msdn.microsoft.com/0d9e1520-6018-425c-a2f9-c408fa3025cf">INetSharingConfiguration::AddPortMapping</a>



<a href="https://msdn.microsoft.com/f5465acc-2b36-47d1-b48f-b36df3a8efb3">INetSharingConfiguration::EnumPortMappings</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

