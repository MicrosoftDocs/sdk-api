---
UID: NS:wincrypt._ROOT_INFO_LUID
title: ROOT_INFO_LUID (wincrypt.h)
author: windows-sdk-content
description: Contains a locally unique identifier (LUID) for Cryptographic Smart Card Root Information.
old-location: security\root_info_luid.htm
tech.root: SecCrypto
ms.assetid: 5b61bbdd-a00a-4985-8066-574f9bff0079
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PROOT_INFO_LUID, PROOT_INFO_LUID, PROOT_INFO_LUID structure pointer [Security], ROOT_INFO_LUID, ROOT_INFO_LUID structure [Security], security.root_info_luid, wincrypt/PROOT_INFO_LUID, wincrypt/ROOT_INFO_LUID"
ms.topic: struct
f1_keywords: 
 - "wincrypt/ROOT_INFO_LUID"
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - ROOT_INFO_LUID
product: Windows
targetos: Windows
req.typenames: ROOT_INFO_LUID, *PROOT_INFO_LUID
req.redist: 
ms.custom: 19H1
---

# ROOT_INFO_LUID structure


## -description


The <b>ROOT_INFO_LUID</b> structure contains a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_luid">LUID</a>) for Cryptographic Smart Card Root Information. The <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crypt_smart_card_root_info">CRYPT_SMART_CARD_ROOT_INFO</a> structure includes a <b>ROOT_INFO_LUID</b> structure.


## -struct-fields




### -field LowPart

Low-order bits.


### -field HighPart

High-order bits.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_luid">LUID</a>
 

 

