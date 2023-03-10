---
UID: NE:ntsecpkg._SECPKG_EXTENDED_INFORMATION_CLASS
title: SECPKG_EXTENDED_INFORMATION_CLASS (ntsecpkg.h)
description: The SECPKG_EXTENDED_INFORMATION_CLASS enumeration describes the type of information to set or get for a security package.This enumeration is used by the SpGetExtendedInformation and SpSetExtendedInformation functions.
helpviewer_keywords: ["SECPKG_EXTENDED_INFORMATION_CLASS","SECPKG_EXTENDED_INFORMATION_CLASS enumeration [Security]","SecpkgContextThunks","SecpkgExtraOids","SecpkgGssInfo","SecpkgMaxInfo","SecpkgMutualAuthLevel","SecpkgNego2Info","SecpkgWowClientDll","_ssp_secpkg_extended_information_class","ntsecpkg/SECPKG_EXTENDED_INFORMATION_CLASS","ntsecpkg/SecpkgContextThunks","ntsecpkg/SecpkgExtraOids","ntsecpkg/SecpkgGssInfo","ntsecpkg/SecpkgMaxInfo","ntsecpkg/SecpkgMutualAuthLevel","ntsecpkg/SecpkgNego2Info","ntsecpkg/SecpkgWowClientDll","security.secpkg_extended_information_class"]
old-location: security\secpkg_extended_information_class.htm
tech.root: security
ms.assetid: 52c24886-ae81-4ac8-97d5-d638016e82bf
ms.date: 12/05/2018
ms.keywords: SECPKG_EXTENDED_INFORMATION_CLASS, SECPKG_EXTENDED_INFORMATION_CLASS enumeration [Security], SecpkgContextThunks, SecpkgExtraOids, SecpkgGssInfo, SecpkgMaxInfo, SecpkgMutualAuthLevel, SecpkgNego2Info, SecpkgWowClientDll, _ssp_secpkg_extended_information_class, ntsecpkg/SECPKG_EXTENDED_INFORMATION_CLASS, ntsecpkg/SecpkgContextThunks, ntsecpkg/SecpkgExtraOids, ntsecpkg/SecpkgGssInfo, ntsecpkg/SecpkgMaxInfo, ntsecpkg/SecpkgMutualAuthLevel, ntsecpkg/SecpkgNego2Info, ntsecpkg/SecpkgWowClientDll, security.secpkg_extended_information_class
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
req.typenames: SECPKG_EXTENDED_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_EXTENDED_INFORMATION_CLASS
 - ntsecpkg/_SECPKG_EXTENDED_INFORMATION_CLASS
 - SECPKG_EXTENDED_INFORMATION_CLASS
 - ntsecpkg/SECPKG_EXTENDED_INFORMATION_CLASS
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
 - SECPKG_EXTENDED_INFORMATION_CLASS
---

# SECPKG_EXTENDED_INFORMATION_CLASS enumeration


## -description

The <b>SECPKG_EXTENDED_INFORMATION_CLASS</b> enumeration describes the type of information to set or get for a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

This enumeration is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -enum-fields

### -field SecpkgGssInfo:1

GSS OID information used to identify the security package in GSS-compatible negotiations.

### -field SecpkgContextThunks

Identifies the calls to the 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function that are handled in the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) process space (LSA mode) rather than being handled in the client process space (user mode).

### -field SecpkgMutualAuthLevel

The mutual authentication level used in the system. This value is valid for the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> function only.

### -field SecpkgWowClientDll

Identifies that the WOW client supports a 32-bit version. Otherwise, the WOW client expects the process to run in 64-bit mode. LSA operations are done by the 64-bit version. When the security context is handed back to the client,  the 32-bit WOW-aware version is loaded and hands it any information from the 64-bit version.

### -field SecpkgExtraOids

Identifies that extra object identifiers (OIDs) are available.

### -field SecpkgMaxInfo

The end value for the enumeration. This value is not a valid parameter value.

### -field SecpkgNego2Info

Identifies the SPNego information for the security package.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This constant is not available.
