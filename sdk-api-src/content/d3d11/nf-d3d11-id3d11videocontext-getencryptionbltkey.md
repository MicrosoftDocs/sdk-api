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
 

 

