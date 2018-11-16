---
UID: NN:netcon.IEnumNetSharingPrivateConnection
title: IEnumNetSharingPrivateConnection
author: windows-sdk-content
description: The IEnumNetSharingPrivateConnection interface provides methods for enumerating the currently configured privately-shared connections.
old-location: ics\ienumnetsharingprivateconnection.htm
tech.root: ICS
ms.assetid: 0e4cfa2e-8caa-4258-bd52-1f5a00403dfa
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumNetSharingPrivateConnection, IEnumNetSharingPrivateConnection interface [ICS/ICF], IEnumNetSharingPrivateConnection interface [ICS/ICF],described, _ics_ienumnetsharingprivateconnection, ics.ienumnetsharingprivateconnection, netcon/IEnumNetSharingPrivateConnection
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
 - IEnumNetSharingPrivateConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNetSharingPrivateConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPrivateConnection</b> interface provides methods for enumerating the currently configured privately-shared connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPrivateConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumNetSharingPrivateConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPrivateConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a82dbc70-783a-4061-9526-dd19f94d843b">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f9cc481-8967-4b1e-95b2-c6ddec20a1ea">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of private connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d68eccf-eb96-47f9-8ca3-97b7918a52fe">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2157ab88-02ed-4c04-be07-7bebe3cd85b8">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of private connections in this enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

