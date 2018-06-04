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

# IDirect3DCryptoSession9::GetEncryptionBltKey


## -description


Gets the cryptographic key used to decrypt the data returned by the <a href="https://msdn.microsoft.com/42aa21d3-7c38-4058-b766-454be8b1ae80">IDirect3DCryptoSession9::EncryptionBlt</a> method.


## -parameters




### -param pReadbackKey

A pointer to a byte array that receives the key. The key is encrypted using the session key.


### -param KeySize

The size of the <i>pReadbackKey</i> array, in bytes. The size should match the size of the session key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method applies only when the driver requires a separate content key for the <a href="https://msdn.microsoft.com/42aa21d3-7c38-4058-b766-454be8b1ae80">EncryptionBlt</a> method. If the driver requires a content key, it sets the <b>D3DCPCAPS_ENCRYPTEDREADBACKKEY</b>
 flag in the capabilities structure returned by the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> method. Otherwise, the driver uses the session key to encrypt the data.

Each time this method is called, the driver generates a new key.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 

