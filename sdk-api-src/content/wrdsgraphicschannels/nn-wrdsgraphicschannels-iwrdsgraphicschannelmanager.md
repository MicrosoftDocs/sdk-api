---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannelManager
title: IWRdsGraphicsChannelManager
author: windows-sdk-content
description: This interface is used by the RemoteFX graphics services API to create the graphics virtual channels necessary for remoting graphics data.
old-location: termserv\iwrdsgraphicschannelmanager.htm
tech.root: TermServ
ms.assetid: 629589cb-9879-491d-a224-6ae2ce8b0ea3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWRdsGraphicsChannelManager, IWRdsGraphicsChannelManager interface [Remote Desktop Services], IWRdsGraphicsChannelManager interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannelmanager, wrdsgraphicschannels/IWRdsGraphicsChannelManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wrdsgraphicschannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
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
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannelManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsGraphicsChannelManager interface


## -description


This interface is used by the RemoteFX graphics services API to create the graphics virtual channels necessary for remoting graphics data. The channel implementer provides a pointer to this interface in the <a href="https://msdn.microsoft.com/70de545f-f630-40cc-8456-ea0703caba17">IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsGraphicsChannelManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsGraphicsChannelManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsGraphicsChannelManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9">CreateChannel</a>
</td>
<td align="left" width="63%">
Used to create a graphics virtual channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/70de545f-f630-40cc-8456-ea0703caba17">IWRdsRemoteFXGraphicsConnection::GetVirtualChannelTransport</a>
 

 

