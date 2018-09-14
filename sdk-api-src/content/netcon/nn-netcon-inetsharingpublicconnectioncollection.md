---
UID: NN:netcon.INetSharingPublicConnectionCollection
title: INetSharingPublicConnectionCollection
author: windows-sdk-content
description: The INetSharingPublicConnectionCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate public connections.
old-location: ics\inetsharingpublicconnectioncollection.htm
tech.root: ICS
ms.assetid: 92027ba2-b803-4c9f-ae77-a89074fef718
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetSharingPublicConnectionCollection, INetSharingPublicConnectionCollection interface [ICS/ICF], INetSharingPublicConnectionCollection interface [ICS/ICF],described, _ics_inetsharingpublicconnectioncollection, ics.inetsharingpublicconnectioncollection, netcon/INetSharingPublicConnectionCollection
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
 - INetSharingPublicConnectionCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingPublicConnectionCollection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingPublicConnectionCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate public connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPublicConnectionCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetSharingPublicConnectionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPublicConnectionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/169de955-d53d-410e-b2e6-911ab0a78bba">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the public connections collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d90ce6c-4ac7-4188-9d25-9144e112a8df">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the public connections collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

