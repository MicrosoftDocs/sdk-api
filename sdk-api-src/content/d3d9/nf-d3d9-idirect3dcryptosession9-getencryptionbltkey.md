---
UID: NF:d3d9.IDirect3DCryptoSession9.GetEncryptionBltKey
title: IDirect3DCryptoSession9::GetEncryptionBltKey
author: windows-sdk-content
description: Gets the cryptographic key used to decrypt the data returned by the IDirect3DCryptoSession9::EncryptionBlt method.
old-location: mf\idirect3dcryptosession9_getencryptionbltkey.htm
old-project: medfound
ms.assetid: c06b42b7-dc8a-4004-b2c5-37accc76db40
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetEncryptionBltKey, GetEncryptionBltKey method [Media Foundation], GetEncryptionBltKey method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetEncryptionBltKey method, IDirect3DCryptoSession9.GetEncryptionBltKey, IDirect3DCryptoSession9::GetEncryptionBltKey, d3d9/IDirect3DCryptoSession9::GetEncryptionBltKey, mf.idirect3dcryptosession9_getencryptionbltkey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.GetEncryptionBltKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

