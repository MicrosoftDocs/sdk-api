---
UID: NN:tsvirtualchannels.IWTSPluginServiceProvider
title: IWTSPluginServiceProvider
author: windows-driver-content
description: Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.
old-location: termserv\iwtspluginserviceprovider.htm
old-project: TermServ
ms.assetid: 8baf8d8b-95a0-46bd-81ea-e99a7db45cdc
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWTSPluginServiceProvider, IWTSPluginServiceProvider interface [Remote Desktop Services], IWTSPluginServiceProvider interface [Remote Desktop Services], described, termserv.iwtspluginserviceprovider, tsvirtualchannels/IWTSPluginServiceProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSVirtualChannels.idl
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
-	tsvirtualchannels.h
api_name:
-	IWTSPluginServiceProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSPluginServiceProvider interface


## -description


Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.

This interface is implemented by the Remote Desktop Connection (RDC) client. You obtain an instance of this interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/289f76b8-dbb5-4f80-98e9-f39f7946494b">IWTSVirtualChannelManager</a> instance obtained in the plug-in's <a href="https://msdn.microsoft.com/9216a069-4fd0-4e88-9cfa-050460b49906">IWTSPlugin::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSPluginServiceProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSPluginServiceProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSPluginServiceProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd99c312-7899-4a94-ad40-abfd1a168332">GetService</a>
</td>
<td align="left" width="63%">
Obtains the specified service.

</td>
</tr>
</table> 

