---
UID: NS:mssip.SIP_INDIRECT_DATA_
title: SIP_INDIRECT_DATA_
author: windows-sdk-content
description: Contains the digest of the hashed subject information.
old-location: security\sip_indirect_data.htm
old-project: SecCrypto
ms.assetid: d34b599b-fe49-47c4-bb52-73ee14d73253
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA, PSIP_INDIRECT_DATA structure pointer [Security], SIP_INDIRECT_DATA, SIP_INDIRECT_DATA structure [Security], SIP_INDIRECT_DATA_, mssip/PSIP_INDIRECT_DATA, mssip/SIP_INDIRECT_DATA, security.sip_indirect_data"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mssip.h
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
req.typenames: SIP_INDIRECT_DATA, *PSIP_INDIRECT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_INDIRECT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SIP_INDIRECT_DATA_ structure


## -description


The <b>SIP_INDIRECT_DATA</b> structure contains the digest of the hashed subject information.


## -struct-fields




### -field Data

A <a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a> structure used to encode the attribute.


### -field DigestAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the digest algorithm to use to create the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>.


### -field Digest

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains the hash of the subject. For information about <b>CRYPT_HASH_BLOB</b>, see <b>CRYPT_INTEGER_BLOB</b>.

