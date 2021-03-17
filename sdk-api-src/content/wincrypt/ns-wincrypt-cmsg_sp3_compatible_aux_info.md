---
UID: NS:wincrypt._CMSG_SP3_COMPATIBLE_AUX_INFO
title: CMSG_SP3_COMPATIBLE_AUX_INFO (wincrypt.h)
description: Contains information needed for SP3 compatible encryption.
helpviewer_keywords: ["*PCMSG_SP3_COMPATIBLE_AUX_INFO","CMSG_SP3_COMPATIBLE_AUX_INFO","CMSG_SP3_COMPATIBLE_AUX_INFO structure [Security]","PCMSG_SP3_COMPATIBLE_AUX_INFO","PCMSG_SP3_COMPATIBLE_AUX_INFO structure pointer [Security]","_crypto2_cmsg_sp3_compatible_aux_info","security.cmsg_sp3_compatible_aux_info","wincrypt/CMSG_SP3_COMPATIBLE_AUX_INFO","wincrypt/PCMSG_SP3_COMPATIBLE_AUX_INFO"]
old-location: security\cmsg_sp3_compatible_aux_info.htm
tech.root: security
ms.assetid: 9afd38c5-fccd-43ea-9c30-c62fdcbee633
ms.date: 12/05/2018
ms.keywords: '*PCMSG_SP3_COMPATIBLE_AUX_INFO, CMSG_SP3_COMPATIBLE_AUX_INFO, CMSG_SP3_COMPATIBLE_AUX_INFO structure [Security], PCMSG_SP3_COMPATIBLE_AUX_INFO, PCMSG_SP3_COMPATIBLE_AUX_INFO structure pointer [Security], _crypto2_cmsg_sp3_compatible_aux_info, security.cmsg_sp3_compatible_aux_info, wincrypt/CMSG_SP3_COMPATIBLE_AUX_INFO, wincrypt/PCMSG_SP3_COMPATIBLE_AUX_INFO'
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
targetos: Windows
req.typenames: CMSG_SP3_COMPATIBLE_AUX_INFO, *PCMSG_SP3_COMPATIBLE_AUX_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_SP3_COMPATIBLE_AUX_INFO
 - wincrypt/_CMSG_SP3_COMPATIBLE_AUX_INFO
 - PCMSG_SP3_COMPATIBLE_AUX_INFO
 - wincrypt/PCMSG_SP3_COMPATIBLE_AUX_INFO
 - CMSG_SP3_COMPATIBLE_AUX_INFO
 - wincrypt/CMSG_SP3_COMPATIBLE_AUX_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_SP3_COMPATIBLE_AUX_INFO
---

# CMSG_SP3_COMPATIBLE_AUX_INFO structure


## -description

The <b>CMSG_SP3_COMPATIBLE_AUX_INFO</b> structure contains information needed for SP3 compatible encryption.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwFlags

Setting CMSG_SP3_COMPATIBLE_ENCRYPT_FLAG enables SP3 compatible encryption. Zero <a href="/windows/desktop/SecGloss/s-gly">salt</a> instead of no salt and the encryption algorithm parameters are <b>NULL</b> instead of containing encoded RC2 parameters or encoded IV octet string. The encrypted <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a> is encoded <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> instead of <a href="/windows/desktop/SecGloss/b-gly">big-endian</a> form.