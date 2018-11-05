---
UID: NF:d3d11.ID3D11VideoContext.ConfigureAuthenticatedChannel
title: ID3D11VideoContext::ConfigureAuthenticatedChannel
author: windows-sdk-content
description: Sends a configuration command to an authenticated channel.
old-location: mf\id3d11videocontext_configureauthenticatedchannel.htm
tech.root: medfound
ms.assetid: 6564EC13-A7B3-4A48-8776-4CD46BFF8E8F
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ConfigureAuthenticatedChannel, ConfigureAuthenticatedChannel method [Media Foundation], ConfigureAuthenticatedChannel method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],ConfigureAuthenticatedChannel method, ID3D11VideoContext.ConfigureAuthenticatedChannel, ID3D11VideoContext::ConfigureAuthenticatedChannel, d3d11/ID3D11VideoContext::ConfigureAuthenticatedChannel, mf.id3d11videocontext_configureauthenticatedchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012, None supported [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - ID3D11VideoContext.ConfigureAuthenticatedChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::ConfigureAuthenticatedChannel


## -description


Sends a configuration command to an authenticated channel.


## -parameters




### -param pChannel [in]

A pointer to the <a href="https://msdn.microsoft.com/B2DE8E06-1571-4D50-9296-8EB4BB74D6BA">ID3D11AuthenticatedChannel</a> interface.


### -param InputSize [in]

The size of the <i>pInput</i> array, in bytes.


### -param pInput [in]

A pointer to a byte array that contains input data for the command. This buffer always starts with a <a href="https://msdn.microsoft.com/11FC071E-9B73-4960-B675-A43DDF75AA0B">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure. The <b>ConfigureType</b> member of the structure specifies the command and defines the meaning of the rest of the buffer.


### -param pOutput [out]

A pointer to a <a href="https://msdn.microsoft.com/68DEC825-5D2E-4A78-B5DD-F7F697BB2980">D3D11_AUTHENTICATED_CONFIGURE_OUTPUT</a> structure that receives the response to the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

