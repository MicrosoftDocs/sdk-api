---
UID: NF:tsvirtualchannels.IWTSPlugin.Terminated
title: IWTSPlugin::Terminated (tsvirtualchannels.h)
description: Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated.
helpviewer_keywords: ["IWTSPlugin interface [Remote Desktop Services]","Terminated method","IWTSPlugin.Terminated","IWTSPlugin::Terminated","Terminated","Terminated method [Remote Desktop Services]","Terminated method [Remote Desktop Services]","IWTSPlugin interface","termserv.iwtsplugin_terminated","tsvirtualchannels/IWTSPlugin::Terminated"]
old-location: termserv\iwtsplugin_terminated.htm
tech.root: TermServ
ms.assetid: face8f79-f02d-465f-b716-1fa170fd6a33
ms.date: 12/05/2018
ms.keywords: IWTSPlugin interface [Remote Desktop Services],Terminated method, IWTSPlugin.Terminated, IWTSPlugin::Terminated, Terminated, Terminated method [Remote Desktop Services], Terminated method [Remote Desktop Services],IWTSPlugin interface, termserv.iwtsplugin_terminated, tsvirtualchannels/IWTSPlugin::Terminated
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
 - IWTSPlugin::Terminated
 - tsvirtualchannels/IWTSPlugin::Terminated
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
 - IWTSPlugin.Terminated
---

# IWTSPlugin::Terminated


## -description

Notifies the plug-in that the Remote Desktop Connection (RDC) client has terminated. After a call is made to <b>IWTSPlugin::Terminated</b>, no other calls to the plug-in are expected. Any plug-in cleanup should be done here.



## -returns

Returns <b>S_OK</b> if the call completes successfully. Results in no action if the call fails.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsplugin">IWTSPlugin</a>
