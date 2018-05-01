---
UID: NN:netcon.INetSharingEveryConnectionCollection
title: INetSharingEveryConnectionCollection
author: windows-driver-content
description: The INetSharingEveryConnectionCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate all the connections in the connections folder.
old-location: ics\inetsharingeveryconnectioncollection.htm
old-project: ICS
ms.assetid: a53c15f0-c7f3-49ea-a85d-663ad4b12f6e
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: INetSharingEveryConnectionCollection, INetSharingEveryConnectionCollection interface [ICS/ICF], INetSharingEveryConnectionCollection interface [ICS/ICF], described, _ics_inetsharingeveryconnectioncollection, ics.inetsharingeveryconnectioncollection, netcon/INetSharingEveryConnectionCollection
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	INetSharingEveryConnectionCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetSharingEveryConnectionCollection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingEveryConnectionCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate all the connections in the connections folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingEveryConnectionCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetSharingEveryConnectionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingEveryConnectionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56d2877b-8e94-4e9a-8d84-5a0263ef825d">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the connections collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c387ab2c-7edd-4975-a735-d555dd7191cf">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the connections collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

