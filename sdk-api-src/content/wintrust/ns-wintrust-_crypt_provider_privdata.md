---
UID: NS:wintrust._CRYPT_PROVIDER_PRIVDATA
title: "_CRYPT_PROVIDER_PRIVDATA"
author: windows-sdk-content
description: Contains private data to be used by a provider.
old-location: security\crypt_provider_privdata.htm
old-project: seccrypto
ms.assetid: 499e4d9b-991a-4317-bc74-a1dfb6609a70
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCRYPT_PROVIDER_PRIVDATA, CRYPT_PROVIDER_PRIVDATA, CRYPT_PROVIDER_PRIVDATA structure [Security], PCRYPT_PROVIDER_PRIVDATA, PCRYPT_PROVIDER_PRIVDATA structure pointer [Security], _CRYPT_PROVIDER_PRIVDATA, security.crypt_provider_privdata, wintrust/CRYPT_PROVIDER_PRIVDATA, wintrust/PCRYPT_PROVIDER_PRIVDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
req.typenames: CRYPT_PROVIDER_PRIVDATA, *PCRYPT_PROVIDER_PRIVDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_PRIVDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CRYPT_PROVIDER_PRIVDATA structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_PRIVDATA</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_PRIVDATA</b> structure contains private data to be used by a provider. The structure is used by the <a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a> structure.


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




<a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a>
 

 

