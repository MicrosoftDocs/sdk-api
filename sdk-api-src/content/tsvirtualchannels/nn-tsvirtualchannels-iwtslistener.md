---
UID: NN:tsvirtualchannels.IWTSListener
title: IWTSListener (tsvirtualchannels.h)
author: windows-sdk-content
description: Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.
old-location: termserv\iwtslistener.htm
tech.root: TermServ
ms.assetid: af0dda9a-0d18-4f44-ac13-0bf2b903d34e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSListener, IWTSListener interface [Remote Desktop Services], IWTSListener interface [Remote Desktop Services],described, termserv.iwtslistener, tsvirtualchannels/IWTSListener
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
 - IWTSListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSListener interface


## -description


Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.

This interface is implemented by the Remote Desktop Connection (RDC) client. A reference is kept typically by the Remote Desktop Connection (RDC) client plug-in. The methods can be executed in any thread that the plug-in chooses. An instance is retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener">IWTSVirtualChannelManager::CreateListener</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSListener</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSListener</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSListener</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtslistener-getconfiguration">GetConfiguration</a>
</td>
<td align="left" width="63%">
Retrieves the listener-specific configuration.

</td>
</tr>
</table> 

