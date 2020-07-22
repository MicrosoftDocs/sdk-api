---
UID: NN:wbemcli.IWbemObjectSinkEx
title: IWbemObjectSinkEx (wbemcli.h)
description: Creates a sink interface that can receive all types of notifications within the WMI programming model.
helpviewer_keywords: ["IWbemObjectSinkEx","IWbemObjectSinkEx interface [Windows Management Instrumentation]","IWbemObjectSinkEx interface [Windows Management Instrumentation]","described","wbemcli/IWbemObjectSinkEx","wmi.iwbemobjectsinkex"]
old-location: wmi\iwbemobjectsinkex.htm
tech.root: wmi
ms.assetid: f22b21f8-5191-480d-8471-3d5fc82ba060
ms.date: 12/05/2018
ms.keywords: IWbemObjectSinkEx, IWbemObjectSinkEx interface [Windows Management Instrumentation], IWbemObjectSinkEx interface [Windows Management Instrumentation],described, wbemcli/IWbemObjectSinkEx, wmi.iwbemobjectsinkex
f1_keywords:
- wbemcli/IWbemObjectSinkEx
dev_langs:
- c++
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
- <TBD>
api_location:
- 
api_name:
- IWbemObjectSinkEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemObjectSinkEx interface


## -description


Creates a sink interface that can receive all types of notifications within the WMI programming model. Clients must implement this interface to receive both the results of the 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/making-an-asynchronous-call-with-c--">asynchronous methods</a> of 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>, and specific types of event notifications. Providers use, but do not implement this interface to provide events and objects to WMI.


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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a>
</td>
<td align="left" width="63%">
Receives notification objects. Inherited from <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsinkex-promptuser">PromptUser</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Called by sources  to indicate the end of a notification sequence, or to send other status codes to the sink. Inherited from <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsinkex-writeerror">WriteError</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsinkex-writemessage">WriteMessage</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsinkex-writeprogress">WriteProgress</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsinkex-writestreamparameter">WriteStreamParameter</a>
</td>
<td align="left" width="63%">
TBD

</td>
</tr>
</table> 

