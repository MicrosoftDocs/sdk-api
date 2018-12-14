---
UID: NS:wincrypt._CRYPT_SMIME_CAPABILITIES
title: CRYPT_SMIME_CAPABILITIES
author: windows-sdk-content
description: Contains a prioritized array of supported capabilities.
old-location: security\crypt_smime_capabilities.htm
tech.root: seccrypto
ms.assetid: 2ee70ff5-4ef4-457c-90c8-629ad0bc3c25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCRYPT_SMIME_CAPABILITIES, CRYPT_SMIME_CAPABILITIES, CRYPT_SMIME_CAPABILITIES structure [Security], PCRYPT_SMIME_CAPABILITIES, PCRYPT_SMIME_CAPABILITIES structure pointer [Security], _crypto2_crypt_smime_capabilities, security.crypt_smime_capabilities, wincrypt/CRYPT_SMIME_CAPABILITIES, wincrypt/PCRYPT_SMIME_CAPABILITIES"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_SMIME_CAPABILITIES
product: Windows
targetos: Windows
req.typenames: CRYPT_SMIME_CAPABILITIES, *PCRYPT_SMIME_CAPABILITIES
req.redist: 
---

# CRYPT_SMIME_CAPABILITIES structure


## -description


The <b>CRYPT_SMIME_CAPABILITIES</b> structure contains a prioritized array of supported capabilities. Capabilities include signature algorithms, <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric algorithms</a>, key enciphering algorithms, and non-algorithm capabilities, which are the preference for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signed data</a> and the preference for unencrypted messages.
<div class="alert"><b>Note</b>  The <b>CRYPT_SMIME_CAPABILITIES</b> are part of an Internet draft proposal. For a complete definition, see "draft-dusse-s/mime-cert-01.txt" dated May 5, 1997.</div><div> </div>

## -struct-fields




### -field cCapability

Count of elements in the <b>rgCapability</b> array.


### -field rgCapability

Prioritized array of pointers to 
<a href="https://msdn.microsoft.com/c7d1e04f-d2b9-4bab-88f4-8a528c527e7c">CRYPT_SMIME_CAPABILITY</a> structures each indicating a capability or preference of a user.


## -see-also




<a href="https://msdn.microsoft.com/c7d1e04f-d2b9-4bab-88f4-8a528c527e7c">CRYPT_SMIME_CAPABILITY</a>
 

 

