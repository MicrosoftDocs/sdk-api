---
UID: NS:wincrypt._CMSG_SP3_COMPATIBLE_AUX_INFO
title: "_CMSG_SP3_COMPATIBLE_AUX_INFO"
author: windows-sdk-content
description: Contains information needed for SP3 compatible encryption.
old-location: security\cmsg_sp3_compatible_aux_info.htm
tech.root: SecCrypto
ms.assetid: 9afd38c5-fccd-43ea-9c30-c62fdcbee633
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCMSG_SP3_COMPATIBLE_AUX_INFO, CMSG_SP3_COMPATIBLE_AUX_INFO, CMSG_SP3_COMPATIBLE_AUX_INFO structure [Security], PCMSG_SP3_COMPATIBLE_AUX_INFO, PCMSG_SP3_COMPATIBLE_AUX_INFO structure pointer [Security], _CMSG_SP3_COMPATIBLE_AUX_INFO, _crypto2_cmsg_sp3_compatible_aux_info, security.cmsg_sp3_compatible_aux_info, wincrypt/CMSG_SP3_COMPATIBLE_AUX_INFO, wincrypt/PCMSG_SP3_COMPATIBLE_AUX_INFO"
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
 - CMSG_SP3_COMPATIBLE_AUX_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_SP3_COMPATIBLE_AUX_INFO, *PCMSG_SP3_COMPATIBLE_AUX_INFO
req.redist: 
---

# _CMSG_SP3_COMPATIBLE_AUX_INFO structure


## -description


The <b>CMSG_SP3_COMPATIBLE_AUX_INFO</b> structure contains information needed for SP3 compatible encryption.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwFlags

Setting CMSG_SP3_COMPATIBLE_ENCRYPT_FLAG enables SP3 compatible encryption. Zero <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">salt</a> instead of no salt and the encryption algorithm parameters are <b>NULL</b> instead of containing encoded RC2 parameters or encoded IV octet string. The encrypted <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> is encoded <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> instead of <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">big-endian</a> form.

