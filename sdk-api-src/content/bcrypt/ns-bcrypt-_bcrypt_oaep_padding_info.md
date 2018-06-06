---
UID: NS:bcrypt._BCRYPT_OAEP_PADDING_INFO
title: "_BCRYPT_OAEP_PADDING_INFO"
author: windows-sdk-content
description: Used to provide options for the Optimal Asymmetric Encryption Padding (OAEP) scheme.
old-location: security\bcrypt_oaep_padding_info.htm
old-project: SecCNG
ms.assetid: 19f48f2d-e952-4a01-8112-f298c79919b2
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: BCRYPT_OAEP_PADDING_INFO, BCRYPT_OAEP_PADDING_INFO structure [Security], _BCRYPT_OAEP_PADDING_INFO, bcrypt/BCRYPT_OAEP_PADDING_INFO, security.bcrypt_oaep_padding_info
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BCRYPT_OAEP_PADDING_INFO
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
req.lib: 
req.dll: 
req.irql: 
---

# _BCRYPT_OAEP_PADDING_INFO structure


## -description


The <b>BCRYPT_OAEP_PADDING_INFO</b> structure is used to provide options for the Optimal Asymmetric Encryption Padding (OAEP) scheme.


## -struct-fields




### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a> to use to create the padding. This algorithm must be a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a>.


### -field pbLabel

The address of a buffer that contains the data to use to create the padding. The <b>cbLabel</b> member contains the size of this buffer.


### -field cbLabel

Contains the number of bytes in the <b>pbLabel</b> buffer to use to create the padding.


## -see-also




<a href="https://msdn.microsoft.com/62286f6b-0d57-4691-83fc-2b9a9740af71">BCryptDecrypt</a>



<a href="https://msdn.microsoft.com/69fe4530-4b7c-40db-a85c-f9dc458735e7">BCryptEncrypt</a>
 

 

