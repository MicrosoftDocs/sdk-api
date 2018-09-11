---
UID: NN:tsvirtualchannels.IWTSVirtualChannelManager
title: IWTSVirtualChannelManager
author: windows-sdk-content
description: Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.
old-location: termserv\iwtsvirtualchannelmanager.htm
tech.root: termserv
ms.assetid: 289f76b8-dbb5-4f80-98e9-f39f7946494b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWTSVirtualChannelManager, IWTSVirtualChannelManager interface [Remote Desktop Services], IWTSVirtualChannelManager interface [Remote Desktop Services],described, termserv.iwtsvirtualchannelmanager, tsvirtualchannels/IWTSVirtualChannelManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IWTSVirtualChannelManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSVirtualChannelManager interface


## -description


Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners. This interface is implemented by the Remote Desktop Connection (RDC) client.

Methods of this interface can be called from any thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSVirtualChannelManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSVirtualChannelManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSVirtualChannelManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62800999-bd13-4529-b5e4-5c6d67d3a6bc">CreateListener</a>
</td>
<td align="left" width="63%">
Returns an instance of a listener object that listens on a specific endpoint, or creates a static channel.

</td>
</tr>
</table> 

