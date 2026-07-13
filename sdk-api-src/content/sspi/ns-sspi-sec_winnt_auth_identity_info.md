---
UID: NS:sspi._SEC_WINNT_AUTH_IDENTITY_INFO
tech.root: security
title: SEC_WINNT_AUTH_IDENTITY_INFO
ms.date: 07/20/2022
targetos: Windows
description: Contains the identity information for authentication.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_WINNT_AUTH_IDENTITY_INFO, *PSEC_WINNT_AUTH_IDENTITY_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_WINNT_AUTH_IDENTITY_INFO
 - PSEC_WINNT_AUTH_IDENTITY_INFO
 - SEC_WINNT_AUTH_IDENTITY_INFO
f1_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_INFO
 - sspi/_SEC_WINNT_AUTH_IDENTITY_INFO
 - PSEC_WINNT_AUTH_IDENTITY_INFO
 - sspi/PSEC_WINNT_AUTH_IDENTITY_INFO
 - SEC_WINNT_AUTH_IDENTITY_INFO
 - sspi/SEC_WINNT_AUTH_IDENTITY_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_WINNT_AUTH_IDENTITY_INFO
---

## -description

Contains the identity information for authentication.

## -struct-fields

### -field AuthIdExw

The **AuthIdExw** authentication identity.

### -field AuthIdExa

The **AuthIdExa** authentication identity.

### -field AuthId_a

The **AuthId_a** authentication identity.

### -field AuthId_w

The **AuthId_w** authentication identity.

### -field AuthIdEx2

The **AuthIdEx2** authentication identity.

## -remarks

How to parse a **SEC_WINNT_AUTH_IDENTITY_INFO** structure:

1. First, check the first **DWORD** of **SEC_WINNT_AUTH_IDENTITY_INFO**. If the first **DWORD** is **0x200**, it is either an **AuthIdExw** or **AuthIdExA**. Otherwise, if the first **DWORD** is **0x201**, the structure is an **AuthIdEx2** structure. Otherwise, the structure is either an **AuthId_a** or an **AuthId_w**.

1. Secondly, check the flags for **SEC_WINNT_AUTH_IDENTITY_ANSI** or **SEC_WINNT_AUTH_IDENTITY_UNICODE**. The presence of the former means the structure is an ANSI structure. Otherwise, the structure is the wide version. Note that **AuthIdEx2** does not have an ANSI version, so this check does not apply to it.

## -see-also
