---
UID: NN:netcon.IEnumNetSharingPublicConnection
title: IEnumNetSharingPublicConnection
author: windows-sdk-content
description: The IEnumNetSharingPublicConnection interface provides methods for enumerating the currently configured publicly-shared connections.
old-location: ics\ienumnetsharingpublicconnection.htm
tech.root: ICS
ms.assetid: 69f2d4c0-7c25-4a50-988b-3ca6babb489a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumNetSharingPublicConnection, IEnumNetSharingPublicConnection interface [ICS/ICF], IEnumNetSharingPublicConnection interface [ICS/ICF],described, _ics_ienumnetsharingpublicconnection, ics.ienumnetsharingpublicconnection, netcon/IEnumNetSharingPublicConnection
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumNetSharingPublicConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNetSharingPublicConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPublicConnection</b> interface provides methods for enumerating the currently configured publicly-shared connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPublicConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumNetSharingPublicConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPublicConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5343acd3-d148-442c-a1d7-226248556f17">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36df4f20-785f-4335-ba75-094533068685">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of public connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f58a9efb-bb0d-477c-946f-5bef6c5635d8">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25466a29-368b-4970-9995-5272cbca3c0a">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of public connections in this enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

