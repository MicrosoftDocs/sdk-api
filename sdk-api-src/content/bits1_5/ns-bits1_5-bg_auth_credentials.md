---
UID: NS:bits1_5.__MIDL_IBackgroundCopyJob2_0003
title: BG_AUTH_CREDENTIALS
description: Identifies the target (proxy or server), authentication scheme, and the user's credentials to use for user authentication requests. The structure is passed to the IBackgroundCopyJob2::SetCredentials method.
helpviewer_keywords: ["*PBG_AUTH_CREDENTIALS","BG_AUTH_CREDENTIALS","BG_AUTH_CREDENTIALS structure [BITS]","_drz_bg_auth_credentials","bits.bg_auth_credentials","bits1_5/BG_AUTH_CREDENTIALS"]
old-location: bits\bg_auth_credentials.htm
tech.root: Bits
ms.assetid: f89ebf46-da83-495c-bafe-b2e0f72f5d8e
ms.date: 12/05/2018
ms.keywords: '*PBG_AUTH_CREDENTIALS, BG_AUTH_CREDENTIALS, BG_AUTH_CREDENTIALS structure [BITS], _drz_bg_auth_credentials, bits.bg_auth_credentials, bits1_5/BG_AUTH_CREDENTIALS'
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
req.typenames: BG_AUTH_CREDENTIALS
req.redist: BITS 1.5 on Windows XP
ms.custom: 19H1
f1_keywords:
 - __MIDL_IBackgroundCopyJob2_0003
 - bits1_5/__MIDL_IBackgroundCopyJob2_0003
 - BG_AUTH_CREDENTIALS
 - bits1_5/BG_AUTH_CREDENTIALS
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
 - BG_AUTH_CREDENTIALS
---

# BG_AUTH_CREDENTIALS structure


## -description

Identifies the target (proxy or server), authentication scheme, and the user's credentials to use for user authentication requests. The structure is passed to the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">IBackgroundCopyJob2::SetCredentials</a> method.

## -struct-fields

### -field Target

Identifies whether to use the credentials for a proxy or server authentication request. For a list of values, see the 
<a href="/windows/desktop/api/bits1_5/ne-bits1_5-bg_auth_target">BG_AUTH_TARGET</a> enumeration. You can specify only one value.

### -field Scheme

Identifies the scheme to use for authentication (for example, Basic or NTLM). For a list of values, see the 
<a href="/windows/desktop/api/bits1_5/ne-bits1_5-bg_auth_scheme">BG_AUTH_SCHEME</a> enumeration. You can specify only one value.

### -field Credentials

Identifies the credentials to use for the specified authentication scheme. For details, see the 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials_union">BG_AUTH_CREDENTIALS_UNION</a> union.

## -see-also

<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials_union">BG_AUTH_CREDENTIALS_UNION</a>



<a href="/windows/desktop/api/bits1_5/ne-bits1_5-bg_auth_scheme">BG_AUTH_SCHEME</a>



<a href="/windows/desktop/api/bits1_5/ne-bits1_5-bg_auth_target">BG_AUTH_TARGET</a>



<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">IBackgroundCopyJob2::SetCredentials</a>