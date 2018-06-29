---
UID: NN:netcon.INetSharingManager
title: INetSharingManager
author: windows-sdk-content
description: The INetSharingManager interface is the primary interface for the Manager object. INetSharingManager provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.
old-location: ics\inetsharingmanager.htm
old-project: ICS
ms.assetid: e7009d13-89c2-4fd9-8f6c-dcdc67178598
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: INetSharingManager, INetSharingManager interface [ICS/ICF], INetSharingManager interface [ICS/ICF],described, _ics_inetsharingmanager, ics.inetsharingmanager, netcon/INetSharingManager
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
 - INetSharingManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingManager interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingManager</b> interface is the primary interface for the Manager object. 
<b>INetSharingManager</b> provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingManager</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetSharingManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f200ffbf-3ce1-4c1b-b4c6-28a8784b5cb8">get_EnumEveryConnection</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for all connections in the connections folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb770e91-0d85-4f67-b7a1-8cc6e89620eb">get_EnumPrivateConnections</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for connections that are privately shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7db0eb73-8e0f-4267-9a88-20952f3721e2">get_EnumPublicConnections</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for connections that are publicly shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">get_INetSharingConfigurationForINetConnection</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface for a specified connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf2db553-f324-4f23-b96e-f8ae703aa3ea">get_NetConnectionProps</a>
</td>
<td align="left" width="63%">
Returns a properties interface for a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cf705dd-41c3-4ac7-a75f-5677a7b49645">get_SharingInstalled</a>
</td>
<td align="left" width="63%">
Reports whether the operating system supports connection sharing.

</td>
</tr>
</table> 


## -remarks



To obtain an enumeration interface for port mappings, use the 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface. Then use the 
<a href="https://msdn.microsoft.com/f5465acc-2b36-47d1-b48f-b36df3a8efb3">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<a href="https://msdn.microsoft.com/68334bd2-353f-457d-a2c7-1271816f10f5">IEnumNetSharingPortMapping</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

