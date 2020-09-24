---
UID: NE:sspi._SECPKG_ATTR_LCT_STATUS
title: SECPKG_ATTR_LCT_STATUS (sspi.h)
description: Indicates whether the token from the most recent call to the InitializeSecurityContext function is the last token from the client.
helpviewer_keywords: ["*PSECPKG_ATTR_LCT_STATUS","SECPKG_ATTR_LCT_STATUS","SECPKG_ATTR_LCT_STATUS enumeration [Security]","SecPkgAttrLastClientTokenMaybe","SecPkgAttrLastClientTokenNo","SecPkgAttrLastClientTokenYes","security.secpkg_attr_lct_status","sspi/SECPKG_ATTR_LCT_STATUS","sspi/SecPkgAttrLastClientTokenMaybe","sspi/SecPkgAttrLastClientTokenNo","sspi/SecPkgAttrLastClientTokenYes"]
old-location: security\secpkg_attr_lct_status.htm
tech.root: security
ms.assetid: b9067862-2339-4543-a8cd-610e6f921bfd
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_ATTR_LCT_STATUS, SECPKG_ATTR_LCT_STATUS, SECPKG_ATTR_LCT_STATUS enumeration [Security], SecPkgAttrLastClientTokenMaybe, SecPkgAttrLastClientTokenNo, SecPkgAttrLastClientTokenYes, security.secpkg_attr_lct_status, sspi/SECPKG_ATTR_LCT_STATUS, sspi/SecPkgAttrLastClientTokenMaybe, sspi/SecPkgAttrLastClientTokenNo, sspi/SecPkgAttrLastClientTokenYes'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SECPKG_ATTR_LCT_STATUS, *PSECPKG_ATTR_LCT_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_ATTR_LCT_STATUS
 - sspi/_SECPKG_ATTR_LCT_STATUS
 - PSECPKG_ATTR_LCT_STATUS
 - sspi/PSECPKG_ATTR_LCT_STATUS
 - SECPKG_ATTR_LCT_STATUS
 - sspi/SECPKG_ATTR_LCT_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SECPKG_ATTR_LCT_STATUS
---

# SECPKG_ATTR_LCT_STATUS enumeration


## -description

Indicates whether the  token from the most recent call to the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> function is the last token from the client.

This enumeration is used in the <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus">SecPkgContext_LastClientTokenStatus</a> structure.

## -enum-fields

### -field SecPkgAttrLastClientTokenYes

The token is the last token from the client.

### -field SecPkgAttrLastClientTokenNo

The token is not the last token from the client.

### -field SecPkgAttrLastClientTokenMaybe

It is not known whether the token is the last token from the client.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus">SecPkgContext_LastClientTokenStatus</a>