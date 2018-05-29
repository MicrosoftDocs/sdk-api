---
UID: NN:netcon.IEnumNetSharingPrivateConnection
title: IEnumNetSharingPrivateConnection
author: windows-sdk-content
description: The IEnumNetSharingPrivateConnection interface provides methods for enumerating the currently configured privately-shared connections.
old-location: ics\ienumnetsharingprivateconnection.htm
old-project: ICS
ms.assetid: 0e4cfa2e-8caa-4258-bd52-1f5a00403dfa
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IEnumNetSharingPrivateConnection, IEnumNetSharingPrivateConnection interface [ICS/ICF], IEnumNetSharingPrivateConnection interface [ICS/ICF],described, _ics_ienumnetsharingprivateconnection, ics.ienumnetsharingprivateconnection, netcon/IEnumNetSharingPrivateConnection
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	IEnumNetSharingPrivateConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of private connections from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
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
 

 

