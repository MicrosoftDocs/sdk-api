---
UID: NN:wbemdisp.ISWbemEventSource
title: ISWbemEventSource
author: windows-sdk-content
description: The SWbemEventSource object retrieves events from an event query in conjunction with SWbemServices.ExecNotificationQuery.
old-location: wmi\swbemeventsource.htm
old-project: WmiSdk
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemEventSource, SWbemEventSource, SWbemEventSource object [Windows Management Instrumentation], SWbemEventSource object [Windows Management Instrumentation],described, _hmm_swbemeventsource, wbemdisp/SWbemEventSource, wmi.swbemeventsource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemEventSource
 - ISWbemEventSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemEventSource interface


## -description


The 
<b>SWbemEventSource</b> object retrieves events from an event query in conjunction with 
<a href="https://msdn.microsoft.com/3e1bb428-5395-4e90-9713-6d96242fef4e">SWbemServices.ExecNotificationQuery</a>. You get an 
<b>SWbemEventSource</b> object if you make a call to <b>SWbemServices.ExecNotificationQuery</b> to make an event query. You can then use the 
<a href="https://msdn.microsoft.com/ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489">NextEvent</a> method to retrieve events as they arrive. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemEventSource</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemEventSource</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489">NextEvent</a>
</td>
<td align="left" width="63%">
Used to retrieve an event in conjunction with <a href="https://msdn.microsoft.com/3e1bb428-5395-4e90-9713-6d96242fef4e">SWbemServices.ExecNotificationQuery</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemEventSource</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9c906b80-ae54-4bc1-a587-43580d6b26e7">Security_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Used to read or change the security settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

