---
UID: NN:netcon.IEnumNetSharingPortMapping
title: IEnumNetSharingPortMapping (netcon.h)
author: windows-sdk-content
description: The IEnumNetSharingPortMapping interface provides methods to enumerate the port mappings for a particular connection.
old-location: ics\ienumnetsharingportmapping.htm
tech.root: ics
ms.assetid: 68334bd2-353f-457d-a2c7-1271816f10f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPortMapping, IEnumNetSharingPortMapping interface [ICS/ICF], IEnumNetSharingPortMapping interface [ICS/ICF],described, _ics_ienumnetsharingportmapping, ics.ienumnetsharingportmapping, netcon/IEnumNetSharingPortMapping
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
 - IEnumNetSharingPortMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNetSharingPortMapping interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPortMapping</b> interface provides methods to enumerate the port mappings for a particular connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPortMapping</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumNetSharingPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d8606ec-d8a2-40c5-9406-fcf16f30e999">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf90fca7-0c4f-474f-a856-7d6865ea8f03">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of port mappings from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d5045b9-a551-4ae5-bd8e-c80e88def237">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b041a1fd-fe33-4519-8ac2-106903c5892f">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of port mappings in this enumeration.

</td>
</tr>
</table> 


## -remarks



To obtain an enumeration interface for port mappings, use the 
<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://msdn.microsoft.com/3ed1a3ae-87af-4415-b149-c66ae65cd053">INetSharingConfiguration</a> interface. Then use the 
<a href="https://msdn.microsoft.com/f5465acc-2b36-47d1-b48f-b36df3a8efb3">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<b>IEnumNetSharingPortMapping</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

