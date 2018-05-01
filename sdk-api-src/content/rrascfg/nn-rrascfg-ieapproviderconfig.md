---
UID: NN:rrascfg.IEAPProviderConfig
title: IEAPProviderConfig
author: windows-driver-content
description: UI for EAP provider.
old-location: eap\ieapproviderconfig.htm
old-project: EAP
ms.assetid: 1e0283b7-ceb3-4c8a-99d9-1a1f1eb5eeb0
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: IEAPProviderConfig, IEAPProviderConfig interface [EAP], IEAPProviderConfig interface [EAP], described, _eap_ieapproviderconfig, eap.ieapproviderconfig, rrascfg/IEAPProviderConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rrascfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProxyFileInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rrascfg.h
api_name:
-	IEAPProviderConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEAPProviderConfig interface


## -description




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEAPProviderConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEAPProviderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEAPProviderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an EAP configuration session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba07f5c6-0b76-489f-b787-2965710cd1c5">RouterInvokeConfigUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP configuration user interface for router-to-router EAP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23b64f95-1f21-4e81-a094-081a95057aef">RouterInvokeCredentialsUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP credentials user interface for router-to-router EAP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95d98664-e108-41d5-8ed0-49867563df43">ServerInvokeConfigUI</a>
</td>
<td align="left" width="63%">
Invokes the EAP configuration user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597582">Uninitialize</a>
</td>
<td align="left" width="63%">
Shuts down an EAP configuration session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1f720c0c-d490-48af-830f-9a25cbc24014">EAP Interfaces</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>
 

 

