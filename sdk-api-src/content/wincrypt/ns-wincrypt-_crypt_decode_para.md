---
UID: NS:wincrypt._CRYPT_DECODE_PARA
title: "_CRYPT_DECODE_PARA"
author: windows-sdk-content
description: Used by the CryptDecodeObjectEx function to provide access to memory allocation and memory freeing callback functions.
old-location: security\crypt_decode_para.htm
old-project: SecCrypto
ms.assetid: 08ed4627-8cbf-415f-b0d0-2c4b9ed9aed1
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PCRYPT_DECODE_PARA, CRYPT_DECODE_PARA, CRYPT_DECODE_PARA structure [Security], PCRYPT_DECODE_PARA, PCRYPT_DECODE_PARA structure pointer [Security], _CRYPT_DECODE_PARA, security.crypt_decode_para, wincrypt/CRYPT_DECODE_PARA, wincrypt/PCRYPT_DECODE_PARA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPT_DECODE_PARA, *PCRYPT_DECODE_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_DECODE_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_DECODE_PARA structure


## -description


The <b>CRYPT_DECODE_PARA</b> structure is used by the <a href="https://msdn.microsoft.com/bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a">CryptDecodeObjectEx</a> function to provide access to memory allocation and memory freeing callback functions.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pfnAlloc

This member is an optional pointer to a callback function used to allocate memory.


### -field pfnFree

This member is an optional pointer to a callback function used to free memory allocated by the allocate callback function.

