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
 

 

