---
UID: NS:bcrypt._BCRYPT_OAEP_PADDING_INFO
title: BCRYPT_OAEP_PADDING_INFO (bcrypt.h)
author: windows-sdk-content
description: Used to provide options for the Optimal Asymmetric Encryption Padding (OAEP) scheme.
old-location: security\bcrypt_oaep_padding_info.htm
tech.root: SecCNG
ms.assetid: 19f48f2d-e952-4a01-8112-f298c79919b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BCRYPT_OAEP_PADDING_INFO, BCRYPT_OAEP_PADDING_INFO structure [Security], bcrypt/BCRYPT_OAEP_PADDING_INFO, security.bcrypt_oaep_padding_info
ms.topic: struct
req.header: bcrypt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_OAEP_PADDING_INFO
product: Windows
targetos: Windows
req.typenames: BCRYPT_OAEP_PADDING_INFO
req.redist: 
ms.custom: 19H1
---

# BCRYPT_OAEP_PADDING_INFO structure


## -description


The <b>BCRYPT_OAEP_PADDING_INFO</b> structure is used to provide options for the Optimal Asymmetric Encryption Padding (OAEP) scheme.


## -struct-fields




### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hashing algorithm</a>.


### -field pbLabel

The address of a buffer that contains the data to use to create the padding. The <b>cbLabel</b> member contains the size of this buffer.


### -field cbLabel

Contains the number of bytes in the <b>pbLabel</b> buffer to use to create the padding.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>
 

 

