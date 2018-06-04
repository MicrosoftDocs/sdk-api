---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Type: <b><a href="https://msdn.microsoft.com/79B63FCD-6BCD-44E6-A5C3-6F5E1336DAA5">WRdsGraphicsChannelType</a></b>

A value of the <a href="https://msdn.microsoft.com/79B63FCD-6BCD-44E6-A5C3-6F5E1336DAA5">WRdsGraphicsChannelType</a> enumeration that specifies what type of channel to create. If the specified type of channel cannot be created, this method should return a channel object rather than fail.


### -param ppVirtualChannel [out, retval]

Type: <b><a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a>**</b>

The address of an <a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a> interface pointer that receives the channel object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/629589cb-9879-491d-a224-6ae2ce8b0ea3">IWRdsGraphicsChannelManager</a>
 

 

