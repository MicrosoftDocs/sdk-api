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

# IDirect3DDevice9Video::CreateAuthenticatedChannel


## -description


Creates a channel to communicate with the Direct3D device or the graphics driver.


## -parameters




### -param ChannelType

Specifies the type of channel, as a member of the <a href="https://msdn.microsoft.com/99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb">D3DAUTHENTICATEDCHANNELTYPE</a> enumeration.


### -param ppAuthenticatedChannel

Receives a pointer to the <a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a> interface. The caller must release the interface.


### -param pChannelHandle

Receives a pointer to a handle for the channel.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>ChannelType</i> parameter is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, the method creates a channel with the Direct3D device. This type of channel does not support authentication.

If <i>ChannelType</i> is <b>D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE</b> or <b>D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE</b>, the method creates an authenticated channel with the graphics driver.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/e2c9cd73-6320-4ce3-a44f-5658c162aeb4">IDirect3DDevice9Video</a>
 

 

