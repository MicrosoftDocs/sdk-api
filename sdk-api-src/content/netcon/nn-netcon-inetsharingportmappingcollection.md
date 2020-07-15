---
UID: NN:netcon.INetSharingPortMappingCollection
title: INetSharingPortMappingCollection (netcon.h)
description: The INetSharingPortMappingCollection interface makes it possible for scripting languages such as VBScript and JScript to enumerate port mappings.
helpviewer_keywords: ["INetSharingPortMappingCollection","INetSharingPortMappingCollection interface [ICS/ICF]","INetSharingPortMappingCollection interface [ICS/ICF]","described","_ics_inetsharingportmappingcollection","ics.inetsharingportmappingcollection","netcon/INetSharingPortMappingCollection"]
old-location: ics\inetsharingportmappingcollection.htm
tech.root: ics
ms.assetid: 09b91df1-b9ef-41b1-b739-65d95f5d60b1
ms.date: 12/05/2018
ms.keywords: INetSharingPortMappingCollection, INetSharingPortMappingCollection interface [ICS/ICF], INetSharingPortMappingCollection interface [ICS/ICF],described, _ics_inetsharingportmappingcollection, ics.inetsharingportmappingcollection, netcon/INetSharingPortMappingCollection
f1_keywords:
- netcon/INetSharingPortMappingCollection
dev_langs:
- c++
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
- INetSharingPortMappingCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingPortMappingCollection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPortMappingCollection</b> interface makes it possible for scripting languages such as VBScript and JScript to enumerate port mappings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMappingCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPortMappingCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingcollection-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the port mapping collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingcollection-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the port mapping collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

