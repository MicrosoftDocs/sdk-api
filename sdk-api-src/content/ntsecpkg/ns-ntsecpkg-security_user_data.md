---
UID: NS:ntsecpkg._SECURITY_USER_DATA
title: SECURITY_USER_DATA (ntsecpkg.h)
description: The SecurityUserData structure contains information about the user of a security support provider/authentication package. This structure is used by the SpGetUserInfo function.
helpviewer_keywords: ["*PSECURITY_USER_DATA","*PSecurityUserData","PSECURITY_USER_DATA","PSECURITY_USER_DATA structure pointer [Security]","PSecurityUserData","PSecurityUserData structure pointer [Security]","SECURITY_USER_DATA","SECURITY_USER_DATA structure [Security]","SecurityUserData","SecurityUserData structure [Security]","_ssp_securityuserdata","ntsecpkg/PSECURITY_USER_DATA","ntsecpkg/PSecurityUserData","ntsecpkg/SecurityUserData","security.securityuserdata"]
old-location: security\securityuserdata.htm
tech.root: security
ms.assetid: 1a56203a-ed6a-4f32-9e7c-b498ba61a64b
ms.date: 12/05/2018
ms.keywords: '*PSECURITY_USER_DATA, *PSecurityUserData, PSECURITY_USER_DATA, PSECURITY_USER_DATA structure pointer [Security], PSecurityUserData, PSecurityUserData structure pointer [Security], SECURITY_USER_DATA, SECURITY_USER_DATA structure [Security], SecurityUserData, SecurityUserData structure [Security], _ssp_securityuserdata, ntsecpkg/PSECURITY_USER_DATA, ntsecpkg/PSecurityUserData, ntsecpkg/SecurityUserData, security.securityuserdata'
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
req.typenames: SECURITY_USER_DATA, *PSECURITY_USER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_USER_DATA
 - ntsecpkg/_SECURITY_USER_DATA
 - PSECURITY_USER_DATA
 - ntsecpkg/PSECURITY_USER_DATA
 - SECURITY_USER_DATA
 - ntsecpkg/SECURITY_USER_DATA
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
 - SECURITY_USER_DATA
---

# SECURITY_USER_DATA structure


## -description

The <b>SecurityUserData</b> structure contains information about the user of a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a>/<a href="/windows/desktop/SecGloss/a-gly">authentication package</a>. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetuserinfofn">SpGetUserInfo</a> function.

## -struct-fields

### -field UserName

The name of the user.

### -field LogonDomainName

The domain the user is logged onto.

### -field LogonServer

The name of the server that logged the user on.

### -field pSid

The <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the user.