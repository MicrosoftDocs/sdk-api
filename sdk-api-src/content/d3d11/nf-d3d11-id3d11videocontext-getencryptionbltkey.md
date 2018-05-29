---
UID: NF:d3d11.ID3D11VideoContext.GetEncryptionBltKey
title: ID3D11VideoContext::GetEncryptionBltKey
author: windows-sdk-content
description: Gets the cryptographic key to decrypt the data returned by the ID3D11VideoContext::EncryptionBlt method.
old-location: mf\id3d11videocontext_getencryptionbltkey.htm
old-project: medfound
ms.assetid: B62BE7CB-75FA-45E9-9AB7-83738DFE3B19
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetEncryptionBltKey, GetEncryptionBltKey method [Media Foundation], GetEncryptionBltKey method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],GetEncryptionBltKey method, ID3D11VideoContext.GetEncryptionBltKey, ID3D11VideoContext::GetEncryptionBltKey, d3d11/ID3D11VideoContext::GetEncryptionBltKey, mf.id3d11videocontext_getencryptionbltkey
ms.prod: windows
ms.technology: windows-sdk
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
-	ID3D11VideoContext.GetEncryptionBltKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::GetEncryptionBltKey


## -description


Gets the cryptographic key to decrypt the data returned by the <a href="https://msdn.microsoft.com/2BBD0BC2-53D9-435E-835C-20A992118329">ID3D11VideoContext::EncryptionBlt</a> method.


## -parameters




### -param pCryptoSession [in]

A pointer to the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface.


### -param KeySize [in]

The size of the <i>pReadbackKey</i> array, in bytes. The size should match the size of the session key.


### -param pReadbackKey [out]

A pointer to a byte array that receives the key. The key is encrypted using the session key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method applies only when the driver requires a separate content key for the <a href="https://msdn.microsoft.com/2BBD0BC2-53D9-435E-835C-20A992118329">EncryptionBlt</a> method. For more information, see the Remarks for <b>EncryptionBlt</b>.

Each time this method is called, the driver generates a new key.

The <i>KeySize</i> should match the size of the session key.

The read back key is encrypted by the driver/hardware using the session key. 




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

