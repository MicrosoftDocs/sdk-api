---
UID: NN:tsvirtualchannels.IWTSVirtualChannelCallback
title: IWTSVirtualChannelCallback
author: windows-driver-content
description: Receives notifications about channel state changes or data received.
old-location: termserv\iwtsvirtualchannelcallback.htm
old-project: TermServ
ms.assetid: d90c6f80-ed4c-4b99-af85-d2c5816ade85
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IWTSVirtualChannelCallback, IWTSVirtualChannelCallback interface [Remote Desktop Services], IWTSVirtualChannelCallback interface [Remote Desktop Services],described, termserv.iwtsvirtualchannelcallback, tsvirtualchannels/IWTSVirtualChannelCallback
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
-	IWTSVirtualChannelCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSVirtualChannelCallback interface


## -description


Receives notifications about channel state changes or data received. This interface is implemented by the user. Each instance of this interface is associated with one instance of <a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a>.

Implementation of this interface should not block these calls, because this may suppress other callbacks. It is not guaranteed that these calls will always arrive on the same thread, even for in-process COM implementation of the plug-in. Calls to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> methods of <a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a> are permitted within these callbacks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSVirtualChannelCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSVirtualChannelCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSVirtualChannelCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5038f2f9-980b-4383-a718-eb4e07e9cfe9">OnClose</a>
</td>
<td align="left" width="63%">
Notifies the user that the channel has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5876ba1a-3f37-4140-b448-91978aa7b0c9">OnDataReceived</a>
</td>
<td align="left" width="63%">
Notifies the user about data that is being received.

</td>
</tr>
</table> 

