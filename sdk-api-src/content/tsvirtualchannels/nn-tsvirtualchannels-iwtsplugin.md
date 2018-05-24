---
UID: NN:tsvirtualchannels.IWTSPlugin
title: IWTSPlugin
author: windows-driver-content
description: Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.
old-location: termserv\iwtsplugin.htm
old-project: TermServ
ms.assetid: e34caf2c-1eb6-40eb-9407-20ed4fde9cdb
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWTSPlugin, IWTSPlugin interface [Remote Desktop Services], IWTSPlugin interface [Remote Desktop Services],described, termserv.iwtsplugin, tsvirtualchannels/IWTSPlugin
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TsVirtualChannels.h
api_name:
-	IWTSPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSPlugin interface


## -description


Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client. The interface is implemented by the plug-in, and is obtained by and managed by the RDC client.

The RDC client obtains an instance of this interface by either instantiating the COM object, or by calling the <a href="https://msdn.microsoft.com/B81BD61E-1F43-42C9-8839-30F4F4C3973C">VirtualChannelGetInstance</a> function implemented by the plug-in. For more information about how the instances are obtained, see <a href="https://msdn.microsoft.com/cda4f8c9-867a-41ac-894a-4296d5912b2b">DVC plug-in registration</a>. In all cases, this instance is kept for the lifetime of the Remote Desktop Connection (RDC) client.

As a COM object, the plug-in must be implemented in a free-threading model. Because the <b>IWTSPlugin</b> methods are implemented by the plug-in, the plug-in must be aware that the call may arrive on different threads. The calls will always arrive serially, so it is impossible to have any two calls that are executed in parallel.

Implementation should not block these calls because this may block other incoming connections or data on existing connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSPlugin</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/089db67e-6c3d-4950-a1dd-de0a3bbe8d5c">Connected</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has successfully connected to the RD Session Host server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbc753b4-531f-476e-8743-b8fbf2481c91">Disconnected</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has disconnected from the RD Session Host server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Used for the first call that is made from the client to the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/face8f79-f02d-465f-b716-1fa170fd6a33">Terminated</a>
</td>
<td align="left" width="63%">
Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated.

</td>
</tr>
</table> 

