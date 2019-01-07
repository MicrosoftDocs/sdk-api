---
UID: NN:sbtsv.ITsSbPluginNotifySink
title: ITsSbPluginNotifySink
author: windows-sdk-content
description: Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about initialization or termination of a plug-in.
old-location: termserv\itssbpluginnotifysink.htm
tech.root: termserv
ms.assetid: c52a3253-74cb-4ff9-a4f3-cb9601c02e7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbPluginNotifySink, ITsSbPluginNotifySink interface [Remote Desktop Services], ITsSbPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbPluginNotifySink, termserv.itssbpluginnotifysink
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbPluginNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbPluginNotifySink interface


## -description


Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about initialization or termination of a plug-in.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbPluginNotifySink</b> interface inherits from <a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>. <b>ITsSbPluginNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbPluginNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fe468c9-457f-4a56-aaf9-4eb48fec8720">OnInitialized</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the plug-in has completed a call of <a href="https://msdn.microsoft.com/1ff0b1a2-042d-4df2-9ae4-cfa4b7c644ab">Initialize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/554139f5-dd20-4bca-8eae-4621535616e6">OnTerminated</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the plug-in has completed a call of <a href="https://msdn.microsoft.com/c47c6231-f967-4239-afd4-a87e9d8f49c2">Terminate</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

