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

# ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange


## -description


Establishes a session key for an authenticated channel.




## -parameters




### -param pChannel [in]

A pointer to the <a href="https://msdn.microsoft.com/B2DE8E06-1571-4D50-9296-8EB4BB74D6BA">ID3D11AuthenticatedChannel</a> interface.  This method will fail if the channel type is    <a href="https://msdn.microsoft.com/4B4E8AA9-5FFE-4ADB-AC83-89FE1BCE27EB">D3D11_AUTHENTICATED_CHANNEL_D3D11</a>, because the Direct3D11 channel does not support authentication.


### -param DataSize [in]

The size of the data in the <i>pData</i> array, in bytes.


### -param pData [in, out]

A pointer to a byte array that contains the encrypted session key. The buffer must contain 256 bytes of data, encrypted using RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP).



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method will fail if the channel type is    <a href="https://msdn.microsoft.com/4B4E8AA9-5FFE-4ADB-AC83-89FE1BCE27EB">D3D11_AUTHENTICATED_CHANNEL_D3D11</a>, because the Direct3D11 channel does not support authentication.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

