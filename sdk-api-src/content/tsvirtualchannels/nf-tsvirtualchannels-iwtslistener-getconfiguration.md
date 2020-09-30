---
UID: NF:tsvirtualchannels.IWTSListener.GetConfiguration
title: IWTSListener::GetConfiguration (tsvirtualchannels.h)
description: Retrieves the listener-specific configuration.
helpviewer_keywords: ["GetConfiguration","GetConfiguration method [Remote Desktop Services]","GetConfiguration method [Remote Desktop Services]","IWTSListener interface","IWTSListener interface [Remote Desktop Services]","GetConfiguration method","IWTSListener.GetConfiguration","IWTSListener::GetConfiguration","termserv.iwtslistener_getconfiguration","tsvirtualchannels/IWTSListener::GetConfiguration"]
old-location: termserv\iwtslistener_getconfiguration.htm
tech.root: TermServ
ms.assetid: 2d45ab39-0a65-4424-b6ea-2a54bb063c0f
ms.date: 12/05/2018
ms.keywords: GetConfiguration, GetConfiguration method [Remote Desktop Services], GetConfiguration method [Remote Desktop Services],IWTSListener interface, IWTSListener interface [Remote Desktop Services],GetConfiguration method, IWTSListener.GetConfiguration, IWTSListener::GetConfiguration, termserv.iwtslistener_getconfiguration, tsvirtualchannels/IWTSListener::GetConfiguration
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
 - IWTSListener::GetConfiguration
 - tsvirtualchannels/IWTSListener::GetConfiguration
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
 - IWTSListener.GetConfiguration
---

# IWTSListener::GetConfiguration


## -description

Retrieves the listener-specific configuration. This configuration is supplied as a <b>BSTR</b> property of the property bag, under the name of <b>WTS_PROPERTY_DEFAULT_CONFIG</b> (which equals the string "DefaultConfig").

## -parameters

### -param ppPropertyBag [out]

Output parameter that receives the property bag.

## -returns

Returns <b>S_OK</b> if successful.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtslistener">IWTSListener</a>