---
UID: NN:tsvirtualchannels.IWTSPluginServiceProvider
title: IWTSPluginServiceProvider (tsvirtualchannels.h)
author: windows-sdk-content
description: Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.
old-location: termserv\iwtspluginserviceprovider.htm
tech.root: TermServ
ms.assetid: 8baf8d8b-95a0-46bd-81ea-e99a7db45cdc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSPluginServiceProvider, IWTSPluginServiceProvider interface [Remote Desktop Services], IWTSPluginServiceProvider interface [Remote Desktop Services],described, termserv.iwtspluginserviceprovider, tsvirtualchannels/IWTSPluginServiceProvider
ms.topic: interface
f1_keywords: ["tsvirtualchannels/IWTSPluginServiceProvider"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tsvirtualchannels.h
api_name:
 - IWTSPluginServiceProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSPluginServiceProvider interface


## -description


Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.

This interface is implemented by the Remote Desktop Connection (RDC) client. You obtain an instance of this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager">IWTSVirtualChannelManager</a> instance obtained in the plug-in's <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsplugin-initialize">IWTSPlugin::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSPluginServiceProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSPluginServiceProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtspluginserviceprovider-getservice">GetService</a>
</td>
<td align="left" width="63%">
Obtains the specified service.

</td>
</tr>
</table> 

