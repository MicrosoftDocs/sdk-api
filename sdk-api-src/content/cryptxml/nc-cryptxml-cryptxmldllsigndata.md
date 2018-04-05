---
UID: NC:cryptxml.CryptXmlDllSignData
title: CryptXmlDllSignData
author: windows-driver-content
description: Signs data.
old-location: security\cryptxmldllsigndata.htm
old-project: SecCrypto
ms.assetid: 6a159fd7-6bf2-43b7-ae7f-b4e4eb02615f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CryptXmlDllSignData, CryptXmlDllSignData function pointer [Security], cryptxml/CryptXmlDllSignData, security.cryptxmldllsigndata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: cryptxml.h
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
req.typenames: CRYPTUI_WIZ_IMPORT_SRC_INFO, *PCRYPTUI_WIZ_IMPORT_SRC_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Cryptxml.h
api_name:
-	CryptXmlDllSignData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CryptXmlDllSignData callback


## -description


The <i>CryptXmlDllSignData</i> function signs data.

The <i>CryptXmlDllSignData</i> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param *pSignatureMethod [in]

A pointer to a <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm.


### -param hCryptProvOrNCryptKey [in]

The handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) that creates the signature. This handle must be an <b>HCRYPTPROV</b> handle that was obtained from a call to the <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that was created by using the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function. New applications should pass in an <a href="https://msdn.microsoft.com/1ad77adb-5960-4965-bddb-5967b982b034">NCRYPT_KEY_HANDLE</a> handle.


### -param dwKeySpec [in]

The private key to use from the provider's container. This key can be AT_KEYEXCHANGE or AT_SIGNATURE. This parameter is ignored if an <b>NCRYPT_KEY_HANDLE</b> handle is used in the <i>hCryptProvOrNCryptKey</i> parameter.


### -param *pbInput [in]

A pointer to a buffer that contains the digest value to sign. The <i>cbInput</i> parameter contains the size of this buffer.


### -param cbInput [in]

The size, in bytes, of the buffer pointed to by the <i>pbInput</i> parameter.


### -param *pbOutput [out, optional]

The address of a buffer to receive the signature produced by this function. The <i>cbOutput</i> parameter contains the size of this buffer.

If this parameter is <b>NULL</b>, this function will calculate the size needed for the encrypted data and return the size in the location pointed to by the <i>pcbResult</i> parameter.


### -param cbOutput [in]

The size, in bytes, of the buffer pointed to by the <i>pbOutput</i> parameter.


### -param *pcbResult [out]

A pointer to a <b>DWORD</b> variable that receives the number of bytes copied to the <i>pbOutput</i> buffer. 
If <i>pbOutput</i> is <b>NULL</b>, this receives the size, in bytes, required for the signature.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



