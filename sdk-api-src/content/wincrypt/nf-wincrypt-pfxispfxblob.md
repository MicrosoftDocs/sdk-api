---
UID: NF:wincrypt.PFXIsPFXBlob
title: PFXIsPFXBlob function
author: windows-sdk-content
description: The PFXIsPFXBlob function attempts to decode the outer layer of a BLOB as a PFX packet.
old-location: security\pfxispfxblob.htm
old-project: SecCrypto
ms.assetid: 28984407-0a28-48e1-9d67-37a6e9db7601
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PFXIsPFXBlob, PFXIsPFXBlob function [Security], _crypto2_pfxispfxblob, security.pfxispfxblob, wincrypt/PFXIsPFXBlob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - PFXIsPFXBlob
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PFXIsPFXBlob function


## -description



			The <b>PFXIsPFXBlob</b> function attempts to decode the outer layer of a BLOB as a PFX packet.


## -parameters




### -param pPFX [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that the function will attempt to decode as a PFX packet.


## -returns



The function returns <b>TRUE</b> if the BLOB can be decoded as a PFX packet. If the outer layer of the BLOB cannot be decoded as a PFX packet, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/47560192-547e-4440-9f10-43327355e1a0">PFXVerifyPassword</a>
 

 

