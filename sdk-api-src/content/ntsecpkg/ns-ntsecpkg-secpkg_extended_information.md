---
UID: NS:ntsecpkg._SECPKG_EXTENDED_INFORMATION
title: SECPKG_EXTENDED_INFORMATION (ntsecpkg.h)
description: The SECPKG_EXTENDED_INFORMATION structure is used to hold information about optional package capabilities.This structure is used by the SpGetExtendedInformation and SpSetExtendedInformation functions.
helpviewer_keywords: ["*PSECPKG_EXTENDED_INFORMATION","PSECPKG_EXTENDED_INFORMATION","PSECPKG_EXTENDED_INFORMATION structure pointer [Security]","SECPKG_EXTENDED_INFORMATION","SECPKG_EXTENDED_INFORMATION structure [Security]","_ssp_secpkg_extended_information","ntsecpkg/PSECPKG_EXTENDED_INFORMATION","ntsecpkg/SECPKG_EXTENDED_INFORMATION","security.secpkg_extended_information"]
old-location: security\secpkg_extended_information.htm
tech.root: security
ms.assetid: 3d80dfc0-c35b-4d14-8196-02944c3db8d2
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_EXTENDED_INFORMATION, PSECPKG_EXTENDED_INFORMATION, PSECPKG_EXTENDED_INFORMATION structure pointer [Security], SECPKG_EXTENDED_INFORMATION, SECPKG_EXTENDED_INFORMATION structure [Security], _ssp_secpkg_extended_information, ntsecpkg/PSECPKG_EXTENDED_INFORMATION, ntsecpkg/SECPKG_EXTENDED_INFORMATION, security.secpkg_extended_information'
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
req.typenames: SECPKG_EXTENDED_INFORMATION, *PSECPKG_EXTENDED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_EXTENDED_INFORMATION
 - ntsecpkg/_SECPKG_EXTENDED_INFORMATION
 - PSECPKG_EXTENDED_INFORMATION
 - ntsecpkg/PSECPKG_EXTENDED_INFORMATION
 - SECPKG_EXTENDED_INFORMATION
 - ntsecpkg/SECPKG_EXTENDED_INFORMATION
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
 - SECPKG_EXTENDED_INFORMATION
---

# SECPKG_EXTENDED_INFORMATION structure


## -description

The <b>SECPKG_EXTENDED_INFORMATION</b> structure is used to hold information about optional package capabilities.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field Class

A value from the 
<a href="/windows/win32/api/ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration which identifies the information in the structure.

### -field Info

Structure that contains the information.

### -field Info.GssInfo

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_gss_info">SECPKG_GSS_INFO</a> structure that contains information used for GSS-compatible negotiations.

### -field Info.ContextThunks

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_context_thunks">SECPKG_CONTEXT_THUNKS</a> structure that contains information about 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> calls to be executed in LSA mode.

### -field Info.MutualAuthLevel

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_mutual_auth_level">SECPKG_MUTUAL_AUTH_LEVEL</a> structure that contains the authentication level used by a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

### -field Info.WowClientDll

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_wow_client_dll">SECPKG_WOW_CLIENT_DLL</a> structure that contains the path to the  WOW client's 32-bit version of the DLL used by a <a href="/windows/desktop/SecGloss/s-gly">security package</a>. LSA operations are done by the 64-bit version. When the security context is handed back to the client,  the 32-bit WOW-aware version is loaded and hands it any information from the 64-bit version.

### -field Info.ExtraOids

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_extra_oids">SECPKG_EXTRA_OIDS</a> structure that contains the extra object identifiers (OIDs) used by a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

### -field Info.Nego2Info

A 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_nego2_info">SECPKG_NEGO2_INFO</a> structure that contains the Nego2 information used by a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.