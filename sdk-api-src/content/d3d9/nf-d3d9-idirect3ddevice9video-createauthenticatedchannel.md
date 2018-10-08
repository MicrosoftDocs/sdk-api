---
UID: NF:d3d9.IDirect3DDevice9Video.CreateAuthenticatedChannel
title: IDirect3DDevice9Video::CreateAuthenticatedChannel
author: windows-sdk-content
description: Creates a channel to communicate with the Direct3D device or the graphics driver.
old-location: mf\idirect3ddevice9video_createauthenticatedchannel.htm
tech.root: medfound
ms.assetid: e0dcfc3f-ede3-4917-8806-6bd343154cf8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateAuthenticatedChannel, CreateAuthenticatedChannel method [Media Foundation], CreateAuthenticatedChannel method [Media Foundation],IDirect3DDevice9Video interface, IDirect3DDevice9Video interface [Media Foundation],CreateAuthenticatedChannel method, IDirect3DDevice9Video.CreateAuthenticatedChannel, IDirect3DDevice9Video::CreateAuthenticatedChannel, d3d9/IDirect3DDevice9Video::CreateAuthenticatedChannel, mf.idirect3ddevice9video_createauthenticatedchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - d3d9.h
api_name:
 - IDirect3DDevice9Video.CreateAuthenticatedChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

