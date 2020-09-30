---
UID: NS:ntsecpkg._SECPKG_CLIENT_INFO
title: SECPKG_CLIENT_INFO (ntsecpkg.h)
description: The SECPKG_CLIENT_INFO structure holds information about a security package's client. This structure is used by the GetClientInfo function.
helpviewer_keywords: ["*PSECPKG_CLIENT_INFO","PSECPKG_CLIENT_INFO","PSECPKG_CLIENT_INFO structure pointer [Security]","SECPKG_CLIENT_INFO","SECPKG_CLIENT_INFO structure [Security]","_ssp_secpkg_client_info","ntsecpkg/PSECPKG_CLIENT_INFO","ntsecpkg/SECPKG_CLIENT_INFO","security.secpkg_client_info"]
old-location: security\secpkg_client_info.htm
tech.root: security
ms.assetid: c9c58a50-7fc2-44a7-9551-a2675410b2b5
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_CLIENT_INFO, PSECPKG_CLIENT_INFO, PSECPKG_CLIENT_INFO structure pointer [Security], SECPKG_CLIENT_INFO, SECPKG_CLIENT_INFO structure [Security], _ssp_secpkg_client_info, ntsecpkg/PSECPKG_CLIENT_INFO, ntsecpkg/SECPKG_CLIENT_INFO, security.secpkg_client_info'
req.header: ntsecpkg.h
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
req.typenames: SECPKG_CLIENT_INFO, *PSECPKG_CLIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_CLIENT_INFO
 - ntsecpkg/_SECPKG_CLIENT_INFO
 - PSECPKG_CLIENT_INFO
 - ntsecpkg/PSECPKG_CLIENT_INFO
 - SECPKG_CLIENT_INFO
 - ntsecpkg/SECPKG_CLIENT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_CLIENT_INFO
---

# SECPKG_CLIENT_INFO structure


## -description

The <b>SECPKG_CLIENT_INFO</b> structure holds information about a <a href="/windows/desktop/SecGloss/s-gly">security package's</a> client. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_client_info">GetClientInfo</a> function.

## -struct-fields

### -field LogonId

The client's effective <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a>.

### -field ProcessID

The client's process identifier.

### -field ThreadID

The client's thread identifier.

### -field HasTcbPrivilege

<b>TRUE</b> if the client has the SeTcbPrivilege privilege; otherwise <b>FALSE</b>.

### -field Impersonating

<b>TRUE</b> if the client is impersonating another <a href="/windows/desktop/SecGloss/s-gly">security principal</a>.

### -field Restricted

The client is restricted in its ability to access securable objects or perform privileged operations.

### -field ClientFlags

### -field ImpersonationLevel

### -field ClientToken