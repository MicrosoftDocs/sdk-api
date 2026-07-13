---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelManager.CreateChannel
title: IWRdsGraphicsChannelManager::CreateChannel (wrdsgraphicschannels.h)
description: Used to create a graphics virtual channel.
helpviewer_keywords: ["CreateChannel","CreateChannel method [Remote Desktop Services]","CreateChannel method [Remote Desktop Services]","IWRdsGraphicsChannelManager interface","IWRdsGraphicsChannelManager interface [Remote Desktop Services]","CreateChannel method","IWRdsGraphicsChannelManager.CreateChannel","IWRdsGraphicsChannelManager::CreateChannel","termserv.iwrdsgraphicschannelmanager_createchannel","wrdsgraphicschannels/IWRdsGraphicsChannelManager::CreateChannel"]
old-location: termserv\iwrdsgraphicschannelmanager_createchannel.htm
tech.root: TermServ
ms.assetid: 2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9
ms.date: 12/05/2018
ms.keywords: CreateChannel, CreateChannel method [Remote Desktop Services], CreateChannel method [Remote Desktop Services],IWRdsGraphicsChannelManager interface, IWRdsGraphicsChannelManager interface [Remote Desktop Services],CreateChannel method, IWRdsGraphicsChannelManager.CreateChannel, IWRdsGraphicsChannelManager::CreateChannel, termserv.iwrdsgraphicschannelmanager_createchannel, wrdsgraphicschannels/IWRdsGraphicsChannelManager::CreateChannel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsGraphicsChannelManager::CreateChannel
 - wrdsgraphicschannels/IWRdsGraphicsChannelManager::CreateChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannelManager.CreateChannel
---

# IWRdsGraphicsChannelManager::CreateChannel


## -description

Used to create a graphics virtual channel.

## -parameters

### -param pszChannelName [in]

Type: <b>const char*</b>

The name of the channel to create. This will be one of the following values.



#### "Microsoft::Windows::RDS::Graphics"

The Remote Desktop graphics channel.



#### "rdpgrfx"

The Remote Desktop information channel.



##### 01"

The video-optimized bitmap remote data channel.



##### 01"

The video-optimized bitmap remote geometry channel.



##### 01"

The video-optimized bitmap remote control channel.

### -param channelType [in]

Type: <b><a href="/windows/win32/api/wrdsgraphicschannels/ne-wrdsgraphicschannels-wrdsgraphicschanneltype">WRdsGraphicsChannelType</a></b>

A value of the <a href="/windows/win32/api/wrdsgraphicschannels/ne-wrdsgraphicschannels-wrdsgraphicschanneltype">WRdsGraphicsChannelType</a> enumeration that specifies what type of channel to create. If the specified type of channel cannot be created, this method should return a channel object rather than fail.

### -param ppVirtualChannel [out, retval]

Type: <b><a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannel">IWRdsGraphicsChannel</a>**</b>

The address of an <a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannel">IWRdsGraphicsChannel</a> interface pointer that receives the channel object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelmanager">IWRdsGraphicsChannelManager</a>