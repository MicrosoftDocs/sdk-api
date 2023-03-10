---
UID: NN:tsvirtualchannels.IWTSPlugin
title: IWTSPlugin (tsvirtualchannels.h)
description: Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.
helpviewer_keywords: ["IWTSPlugin","IWTSPlugin interface [Remote Desktop Services]","IWTSPlugin interface [Remote Desktop Services]","described","termserv.iwtsplugin","tsvirtualchannels/IWTSPlugin"]
old-location: termserv\iwtsplugin.htm
tech.root: TermServ
ms.assetid: e34caf2c-1eb6-40eb-9407-20ed4fde9cdb
ms.date: 12/05/2018
ms.keywords: IWTSPlugin, IWTSPlugin interface [Remote Desktop Services], IWTSPlugin interface [Remote Desktop Services],described, termserv.iwtsplugin, tsvirtualchannels/IWTSPlugin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSPlugin
 - tsvirtualchannels/IWTSPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSPlugin
---

# IWTSPlugin interface


## -description

Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client. The interface is implemented by the plug-in, and is obtained by and managed by the RDC client.

The RDC client obtains an instance of this interface by either instantiating the COM object, or by calling the <a href="/windows/desktop/TermServ/virtualchannelgetinstance">VirtualChannelGetInstance</a> function implemented by the plug-in. For more information about how the instances are obtained, see <a href="/windows/desktop/TermServ/dvc-plug-in-registration">DVC plug-in registration</a>. In all cases, this instance is kept for the lifetime of the Remote Desktop Connection (RDC) client.

As a COM object, the plug-in must be implemented in a free-threading model. Because the <b>IWTSPlugin</b> methods are implemented by the plug-in, the plug-in must be aware that the call may arrive on different threads. The calls will always arrive serially, so it is impossible to have any two calls that are executed in parallel.

Implementation should not block these calls because this may block other incoming connections or data on existing connections.

## -inheritance

The <b>IWTSPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSPlugin</b> also has these types of members:

## -remarks

The **IWTSPlugin** interface is implemented by %System32%\webauthn.dll to enable the Remote Desktop WebAuthn redirection functionality. Get an instance of this interface by calling [VirtualChannelGetInstance]( ../termserv/virtualchannelgetinstance.md), which is also provided by webauthn.dll.
