---
UID: NN:sbtsv.ITsSbPluginNotifySink
title: ITsSbPluginNotifySink (sbtsv.h)
description: Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about initialization or termination of a plug-in.
helpviewer_keywords: ["ITsSbPluginNotifySink","ITsSbPluginNotifySink interface [Remote Desktop Services]","ITsSbPluginNotifySink interface [Remote Desktop Services]","described","sbtsv/ITsSbPluginNotifySink","termserv.itssbpluginnotifysink"]
old-location: termserv\itssbpluginnotifysink.htm
tech.root: TermServ
ms.assetid: c52a3253-74cb-4ff9-a4f3-cb9601c02e7d
ms.date: 12/05/2018
ms.keywords: ITsSbPluginNotifySink, ITsSbPluginNotifySink interface [Remote Desktop Services], ITsSbPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbPluginNotifySink, termserv.itssbpluginnotifysink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbPluginNotifySink
 - sbtsv/ITsSbPluginNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbPluginNotifySink
---

# ITsSbPluginNotifySink interface


## -description

Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about initialization or termination of a plug-in.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbPluginNotifySink</b> interface inherits from <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>. <b>ITsSbPluginNotifySink</b> also has these types of members:
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
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbpluginnotifysink-oninitialized">OnInitialized</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the plug-in has completed a call of <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplugin-initialize">Initialize</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbpluginnotifysink-onterminated">OnTerminated</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the plug-in has completed a call of <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplugin-terminate">Terminate</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>