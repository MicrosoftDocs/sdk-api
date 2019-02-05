---
UID: NN:wbemcli.IWbemObjectSinkEx
title: IWbemObjectSinkEx
author: windows-sdk-content
description: Creates a sink interface that can receive all types of notifications within the WMI programming model.
old-location: wmi\iwbemobjectsinkex.htm
tech.root: WmiSdk
ms.assetid: f22b21f8-5191-480d-8471-3d5fc82ba060
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemObjectSinkEx, IWbemObjectSinkEx interface [Windows Management Instrumentation], IWbemObjectSinkEx interface [Windows Management Instrumentation],described, wbemcli/IWbemObjectSinkEx, wmi.iwbemobjectsinkex
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
topic_type:
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 -
api_name:
 - IWbemObjectSinkEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemObjectSinkEx interface


## -description


Creates a sink interface that can receive all types of notifications within the WMI programming model. Clients must implement this interface to receive both the results of the 
<a href="https://msdn.microsoft.com/5179969f-bc7d-4408-84ef-7b003950a59f">asynchronous methods</a> of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>, and specific types of event notifications. Providers use, but do not implement this interface to provide events and objects to WMI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemObjectSinkEx</b> interface inherits from <b>IWbemObjectSink</b>. <b>IWbemObjectSinkEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemObjectSinkEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa391788(v=VS.85).aspx">Indicate</a>
</td>
<td align="left" width="63%">
Receives notification objects. Inherited from <a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4ea6f73-e94f-4ffa-9528-43b52ab00192">PromptUser</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa391789(v=VS.85).aspx">SetStatus</a>
</td>
<td align="left" width="63%">
Called by sources  to indicate the end of a notification sequence, or to send other status codes to the sink. Inherited from <a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/908b46de-a64e-4db0-957f-6aeb4870ad46">WriteError</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b9df753-9148-4578-8265-2cb85526bdc9">WriteMessage</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78323321-942d-47f2-82e6-19ae2ea39b6a">WriteProgress</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/609ed388-3d6a-49ba-91ae-78a34bddd100">WriteStreamParameter</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
</table> 

