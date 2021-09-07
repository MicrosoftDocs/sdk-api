---
UID: NF:d3d11.ID3D11VideoDevice.CreateAuthenticatedChannel
title: ID3D11VideoDevice::CreateAuthenticatedChannel (d3d11.h)
description: Creates a channel to communicate with the Microsoft Direct3D device or the graphics driver.
helpviewer_keywords: ["CreateAuthenticatedChannel","CreateAuthenticatedChannel method [Media Foundation]","CreateAuthenticatedChannel method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CreateAuthenticatedChannel method","ID3D11VideoDevice.CreateAuthenticatedChannel","ID3D11VideoDevice::CreateAuthenticatedChannel","d3d11/ID3D11VideoDevice::CreateAuthenticatedChannel","mf.id3d11videodevice_createauthenticatedchannel"]
old-location: mf\id3d11videodevice_createauthenticatedchannel.htm
tech.root: mf
ms.assetid: 4325E83F-23BF-4104-B30E-27DBE7D23D88
ms.date: 12/05/2018
ms.keywords: CreateAuthenticatedChannel, CreateAuthenticatedChannel method [Media Foundation], CreateAuthenticatedChannel method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateAuthenticatedChannel method, ID3D11VideoDevice.CreateAuthenticatedChannel, ID3D11VideoDevice::CreateAuthenticatedChannel, d3d11/ID3D11VideoDevice::CreateAuthenticatedChannel, mf.id3d11videodevice_createauthenticatedchannel
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoDevice::CreateAuthenticatedChannel
 - d3d11/ID3D11VideoDevice::CreateAuthenticatedChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.CreateAuthenticatedChannel
---

# ID3D11VideoDevice::CreateAuthenticatedChannel


## -description

Creates a channel to communicate with the Microsoft Direct3D device or the graphics driver. The channel can be used to send commands and queries for content protection.

## -parameters

### -param ChannelType [in]

Specifies the type of channel, as a member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_authenticated_channel_type">D3D11_AUTHENTICATED_CHANNEL_TYPE</a> enumeration.

### -param ppAuthenticatedChannel [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>ChannelType</i> parameter is <b>D3D11_AUTHENTICATED_CHANNEL_D3D11</b>, the method creates a channel with the Direct3D device. This type of channel does not support authentication.

If <i>ChannelType</i> is <b>D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE</b> or <b>D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE</b>, the method creates an authenticated channel with the graphics driver.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>