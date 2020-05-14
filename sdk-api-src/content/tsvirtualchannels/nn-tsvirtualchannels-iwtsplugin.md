---
UID: NN:tsvirtualchannels.IWTSPlugin
title: IWTSPlugin (tsvirtualchannels.h)
description: Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.helpviewer_keywords: ["IWTSPlugin","IWTSPlugin interface [Remote Desktop Services]","IWTSPlugin interface [Remote Desktop Services]","described","termserv.iwtsplugin","tsvirtualchannels/IWTSPlugin"]
old-location: termserv\iwtsplugin.htm
tech.root: TermServ
ms.assetid: e34caf2c-1eb6-40eb-9407-20ed4fde9cdb
ms.date: 12/05/2018
ms.keywords: IWTSPlugin, IWTSPlugin interface [Remote Desktop Services], IWTSPlugin interface [Remote Desktop Services],described, termserv.iwtsplugin, tsvirtualchannels/IWTSPlugin
f1_keywords:
- tsvirtualchannels/IWTSPlugin
dev_langs:
- c++
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
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
- TsVirtualChannels.h
api_name:
- IWTSPlugin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSPlugin interface


## -description


Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client. The interface is implemented by the plug-in, and is obtained by and managed by the RDC client.

The RDC client obtains an instance of this interface by either instantiating the COM object, or by calling the <a href="https://docs.microsoft.com/windows/desktop/TermServ/virtualchannelgetinstance">VirtualChannelGetInstance</a> function implemented by the plug-in. For more information about how the instances are obtained, see <a href="https://docs.microsoft.com/windows/desktop/TermServ/dvc-plug-in-registration">DVC plug-in registration</a>. In all cases, this instance is kept for the lifetime of the Remote Desktop Connection (RDC) client.

As a COM object, the plug-in must be implemented in a free-threading model. Because the <b>IWTSPlugin</b> methods are implemented by the plug-in, the plug-in must be aware that the call may arrive on different threads. The calls will always arrive serially, so it is impossible to have any two calls that are executed in parallel.

Implementation should not block these calls because this may block other incoming connections or data on existing connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSPlugin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsplugin-connected">Connected</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has successfully connected to the RD Session Host server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsplugin-disconnected">Disconnected</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the RD Session Host server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsplugin-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Used for the first call that is made from the client to the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsplugin-terminated">Terminated</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated.

</td>
</tr>
</table> 

