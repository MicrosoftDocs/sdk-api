---
UID: NS:ncrypt.__NCRYPT_SUPPORTED_LENGTHS
title: "__NCRYPT_SUPPORTED_LENGTHS"
author: windows-sdk-content
description: Used with the NCRYPT_LENGTHS_PROPERTY property to contain length information for a key.
old-location: security\ncrypt_supported_lengths.htm
old-project: SecCNG
ms.assetid: 11bb3669-d536-4c8f-a30b-1826ccdbe275
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: NCRYPT_SUPPORTED_LENGTHS, NCRYPT_SUPPORTED_LENGTHS structure [Security], __NCRYPT_SUPPORTED_LENGTHS, ncrypt/NCRYPT_SUPPORTED_LENGTHS, security.ncrypt_supported_lengths
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NCRYPT_SUPPORTED_LENGTHS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ncrypt.h
api_name:
-	NCRYPT_SUPPORTED_LENGTHS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __NCRYPT_SUPPORTED_LENGTHS structure


## -description


The <b>NCRYPT_SUPPORTED_LENGTHS</b> structure is used with the <a href="https://msdn.microsoft.com/407f0e42-07c8-4ec6-81c6-f8bde005adb0">NCRYPT_LENGTHS_PROPERTY</a> property to contain length information for a key.


## -struct-fields




### -field dwMinLength

The minimum length, in bits, of a key.


### -field dwMaxLength

The maximum length, in bits, of a key.


### -field dwIncrement

The number of bits that the key size can be incremented between <b>dwMinLength</b> and <b>dwMaxLength</b>.


### -field dwDefaultLength

The default length, in bits, of a key.

