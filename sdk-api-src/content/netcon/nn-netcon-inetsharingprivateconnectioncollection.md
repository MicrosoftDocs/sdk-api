---
UID: NN:netcon.INetSharingPrivateConnectionCollection
title: INetSharingPrivateConnectionCollection
author: windows-sdk-content
description: The INetSharingPrivateConnectionCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate private connections.
old-location: ics\inetsharingprivateconnectioncollection.htm
tech.root: ICS
ms.assetid: 6e850e7b-841a-4f14-bab2-4a5a67dcb360
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetSharingPrivateConnectionCollection, INetSharingPrivateConnectionCollection interface [ICS/ICF], INetSharingPrivateConnectionCollection interface [ICS/ICF],described, _ics_inetsharingprivateconnectioncollection, ics.inetsharingprivateconnectioncollection, netcon/INetSharingPrivateConnectionCollection
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
 - INetSharingPrivateConnectionCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetSharingPrivateConnectionCollection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingPrivateConnectionCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate private connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPrivateConnectionCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetSharingPrivateConnectionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPrivateConnectionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/526da220-5999-4b84-b617-26edf23c15ab">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the private connections collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/599ffa10-6932-48bd-a736-60512f25271c">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the private connections collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

