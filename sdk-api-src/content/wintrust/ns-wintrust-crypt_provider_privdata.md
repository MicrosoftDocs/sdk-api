---
UID: NS:wintrust._CRYPT_PROVIDER_PRIVDATA
title: CRYPT_PROVIDER_PRIVDATA (wintrust.h)
author: windows-sdk-content
description: Contains private data to be used by a provider.
old-location: security\crypt_provider_privdata.htm
tech.root: SecCrypto
ms.assetid: 499e4d9b-991a-4317-bc74-a1dfb6609a70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_PRIVDATA, CRYPT_PROVIDER_PRIVDATA, CRYPT_PROVIDER_PRIVDATA structure [Security], PCRYPT_PROVIDER_PRIVDATA, PCRYPT_PROVIDER_PRIVDATA structure pointer [Security], security.crypt_provider_privdata, wintrust/CRYPT_PROVIDER_PRIVDATA, wintrust/PCRYPT_PROVIDER_PRIVDATA'
ms.topic: struct
f1_keywords:
- wintrust/CRYPT_PROVIDER_PRIVDATA
req.header: wintrust.h
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
- Wintrust.h
api_name:
- CRYPT_PROVIDER_PRIVDATA
targetos: Windows
req.typenames: CRYPT_PROVIDER_PRIVDATA, *PCRYPT_PROVIDER_PRIVDATA
req.redist: 
ms.custom: 19H1
---

# CRYPT_PROVIDER_PRIVDATA structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_PRIVDATA</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_PRIVDATA</b> structure contains private data to be used by a provider. The structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field gProviderID

<b>GUID</b> that identifies the provider.


### -field cbProvData

Number of bytes referenced by <b>pvProvData</b>.


### -field pvProvData

A pointer to a <b>void</b> that contains the private data.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a>
 

 

