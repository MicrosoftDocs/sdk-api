---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelManager.CreateChannel
title: IWRdsGraphicsChannelManager::CreateChannel (wrdsgraphicschannels.h)
author: windows-sdk-content
description: Used to create a graphics virtual channel.
old-location: termserv\iwrdsgraphicschannelmanager_createchannel.htm
tech.root: TermServ
ms.assetid: 2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateChannel, CreateChannel method [Remote Desktop Services], CreateChannel method [Remote Desktop Services],IWRdsGraphicsChannelManager interface, IWRdsGraphicsChannelManager interface [Remote Desktop Services],CreateChannel method, IWRdsGraphicsChannelManager.CreateChannel, IWRdsGraphicsChannelManager::CreateChannel, termserv.iwrdsgraphicschannelmanager_createchannel, wrdsgraphicschannels/IWRdsGraphicsChannelManager::CreateChannel
ms.topic: method
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
 - IWRdsGraphicsChannelManager.CreateChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/JJ219269(v=VS.85).aspx">WRdsGraphicsChannelType</a></b>

A value of the <a href="https://msdn.microsoft.com/en-us/library/JJ219269(v=VS.85).aspx">WRdsGraphicsChannelType</a> enumeration that specifies what type of channel to create. If the specified type of channel cannot be created, this method should return a channel object rather than fail.


### -param ppVirtualChannel [out, retval]

Type: <b><a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a>**</b>

The address of an <a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a> interface pointer that receives the channel object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/629589cb-9879-491d-a224-6ae2ce8b0ea3">IWRdsGraphicsChannelManager</a>
 

 

