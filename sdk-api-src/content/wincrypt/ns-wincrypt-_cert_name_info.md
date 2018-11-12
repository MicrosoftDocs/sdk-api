---
UID: NS:wincrypt._CERT_NAME_INFO
title: "_CERT_NAME_INFO"
author: windows-sdk-content
description: Contains subject or issuer names.
old-location: security\cert_name_info.htm
tech.root: seccrypto
ms.assetid: 402d1051-d91a-4a79-96f6-10ed96a32d5c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCERT_NAME_INFO, CERT_NAME_INFO, CERT_NAME_INFO structure [Security], PCERT_NAME_INFO, PCERT_NAME_INFO structure pointer [Security], _CERT_NAME_INFO, _crypto2_cert_name_info, security.cert_name_info, wincrypt/CERT_NAME_INFO, wincrypt/PCERT_NAME_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
 - CERT_NAME_INFO
product: Windows
targetos: Windows
req.typenames: CERT_NAME_INFO, *PCERT_NAME_INFO
req.redist: 
---

# _CERT_NAME_INFO structure


## -description


The <b>CERT_NAME_INFO</b> structure contains subject or issuer names. The information is represented as an array of 
<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> structures.


## -struct-fields




### -field cRDN

Number of elements in the <b>rgRDN</b> array.


### -field rgRDN

Array of pointers to 
<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a>



<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>
 

 

