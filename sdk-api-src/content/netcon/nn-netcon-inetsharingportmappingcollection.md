---
UID: NN:netcon.INetSharingPortMappingCollection
title: INetSharingPortMappingCollection
author: windows-sdk-content
description: The INetSharingPortMappingCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate port mappings.
old-location: ics\inetsharingportmappingcollection.htm
old-project: ics
ms.assetid: 09b91df1-b9ef-41b1-b739-65d95f5d60b1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetSharingPortMappingCollection, INetSharingPortMappingCollection interface [ICS/ICF], INetSharingPortMappingCollection interface [ICS/ICF],described, _ics_inetsharingportmappingcollection, ics.inetsharingportmappingcollection, netcon/INetSharingPortMappingCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: netcon.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingPortMappingCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingPortMappingCollection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingPortMappingCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate port mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMappingCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetSharingPortMappingCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPortMappingCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e7fee0-70b7-4b74-a95f-0637a0c1cdd2">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the port mapping collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40a697e8-aac4-4656-9c86-d11b5cdcb9e2">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the port mapping collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/68334bd2-353f-457d-a2c7-1271816f10f5">IEnumNetSharingPortMapping</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

