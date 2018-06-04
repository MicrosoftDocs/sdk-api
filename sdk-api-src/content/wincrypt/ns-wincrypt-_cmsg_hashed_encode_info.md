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

# _CMSG_HASHED_ENCODE_INFO structure


## -description


The <b>CMSG_HASHED_ENCODE_INFO</b> structure is used with <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashed</a> messages. It is passed to 
the <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> function if the <b>CryptMsgOpenToEncode</b> function's <i>dwMsgType</i> parameter is <b>CMSG_ENVELOPED</b>.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Specifies a handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) used to do the hash. The <i>hCryptProv</i> private keys are not used. 


This member's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, pass zero to use the default RSA or DSS provider to be acquired before doing hash, signature verification, or recipient encryption operations.




### -field HashAlgorithm


						A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the hash algorithm type and any associated additional parameters.


### -field pvHashAuxInfo

This member is currently not used and must be set to <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>
 

 

