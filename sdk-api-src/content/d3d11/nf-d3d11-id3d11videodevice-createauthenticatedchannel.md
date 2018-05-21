---
UID: NF:d3d11.ID3D11VideoDevice.CreateAuthenticatedChannel
title: ID3D11VideoDevice::CreateAuthenticatedChannel
author: windows-driver-content
description: Creates a channel to communicate with the Microsoft Direct3D device or the graphics driver.
old-location: mf\id3d11videodevice_createauthenticatedchannel.htm
old-project: medfound
ms.assetid: 4325E83F-23BF-4104-B30E-27DBE7D23D88
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: CreateAuthenticatedChannel, CreateAuthenticatedChannel method [Media Foundation], CreateAuthenticatedChannel method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateAuthenticatedChannel method, ID3D11VideoDevice.CreateAuthenticatedChannel, ID3D11VideoDevice::CreateAuthenticatedChannel, d3d11/ID3D11VideoDevice::CreateAuthenticatedChannel, mf.id3d11videodevice_createauthenticatedchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoDevice.CreateAuthenticatedChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoDevice::CreateAuthenticatedChannel


## -description


Creates a channel to communicate with the Microsoft Direct3D device or the graphics driver. The channel can be used to send commands and queries for content protection.


## -parameters




### -param ChannelType [in]

Specifies the type of channel, as a member of the <a href="https://msdn.microsoft.com/4B4E8AA9-5FFE-4ADB-AC83-89FE1BCE27EB">D3D11_AUTHENTICATED_CHANNEL_TYPE</a> enumeration.


### -param ppAuthenticatedChannel [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/B2DE8E06-1571-4D50-9296-8EB4BB74D6BA">ID3D11AuthenticatedChannel</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>ChannelType</i> parameter is <b>D3D11_AUTHENTICATED_CHANNEL_D3D11</b>, the method creates a channel with the Direct3D device. This type of channel does not support authentication.

If <i>ChannelType</i> is <b>D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE</b> or <b>D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE</b>, the method creates an authenticated channel with the graphics driver.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

