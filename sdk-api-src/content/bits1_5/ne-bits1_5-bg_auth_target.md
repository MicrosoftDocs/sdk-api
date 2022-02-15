---
UID: NE:bits1_5.BG_AUTH_TARGET
title: BG_AUTH_TARGET
description: Defines constants that specify whether the credentials are used for proxy or server user authentication requests.
helpviewer_keywords: ["BG_AUTH_TARGET","BG_AUTH_TARGET enumeration [BITS]","BG_AUTH_TARGET_PROXY","BG_AUTH_TARGET_SERVER","_drz_bg_auth_target","bits.bg_auth_target","bits1_5/BG_AUTH_TARGET","bits1_5/BG_AUTH_TARGET_PROXY","bits1_5/BG_AUTH_TARGET_SERVER"]
old-location: bits\bg_auth_target.htm
tech.root: Bits
ms.assetid: efe7aa0a-48fc-4192-b81b-40d3a9b0fb22
ms.date: 02/20/2019
ms.keywords: BG_AUTH_TARGET, BG_AUTH_TARGET enumeration [BITS], BG_AUTH_TARGET_PROXY, BG_AUTH_TARGET_SERVER, _drz_bg_auth_target, bits.bg_auth_target, bits1_5/BG_AUTH_TARGET, bits1_5/BG_AUTH_TARGET_PROXY, bits1_5/BG_AUTH_TARGET_SERVER
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_AUTH_TARGET
req.redist: BITS 1.5 on  Windows XP
f1_keywords:
 - BG_AUTH_TARGET
 - bits1_5/BG_AUTH_TARGET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits1_5.h
api_name:
 - BG_AUTH_TARGET
---

# BG_AUTH_TARGET enumeration


## -description

Defines constants that specify whether the credentials are used for proxy or server user authentication requests.

## -enum-fields

### -field BG_AUTH_TARGET_SERVER:1

Use credentials for server requests.

### -field BG_AUTH_TARGET_PROXY

Use credentials for proxy requests.

## -see-also

* [BG_AUTH_CREDENTIALS structure](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials)
* [IBackgroundCopyJob2::RemoveCredentials method](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-removecredentials)

