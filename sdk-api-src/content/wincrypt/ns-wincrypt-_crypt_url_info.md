---
UID: NS:wincrypt._CRYPT_URL_INFO
title: "_CRYPT_URL_INFO"
author: windows-sdk-content
description: Contains information about groupings of URLs.
old-location: security\crypt_url_info.htm
tech.root: seccrypto
ms.assetid: 58289a66-6580-468c-b001-5da08cf6d4a9
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PCRYPT_URL_INFO, CRYPT_URL_INFO, CRYPT_URL_INFO structure [Security], PCRYPT_URL_INFO, PCRYPT_URL_INFO structure pointer [Security], _CRYPT_URL_INFO, _crypto2_crypt_url_info, security.crypt_url_info, wincrypt/CRYPT_URL_INFO, wincrypt/PCRYPT_URL_INFO"
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
 - CRYPT_URL_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_URL_INFO, *PCRYPT_URL_INFO
req.redist: 
---

# _CRYPT_URL_INFO structure


## -description


The <b>CRYPT_URL_INFO</b> structure contains information about groupings of URLs.


## -struct-fields




### -field cbSize

The size, in bytes, of the structure.


### -field dwSyncDeltaTime

Number of seconds between synchronizations.


### -field cGroup

Number of elements in the rgcGroupEntry array of URL groups.


### -field rgcGroupEntry

Array of URL groups returned.

