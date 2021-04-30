---
UID: NS:ntsecpkg._SECPKG_GSS_INFO
title: SECPKG_GSS_INFO (ntsecpkg.h)
description: A SECPKG_GSS_INFO structure contains information used for GSS-compatible negotiations.
helpviewer_keywords: ["*PSECPKG_GSS_INFO","PSECPKG_GSS_INFO","PSECPKG_GSS_INFO structure pointer [Security]","SECPKG_GSS_INFO","SECPKG_GSS_INFO structure [Security]","_ssp_secpkg_gss_info","ntsecpkg/PSECPKG_GSS_INFO","ntsecpkg/SECPKG_GSS_INFO","security.secpkg_gss_info"]
old-location: security\secpkg_gss_info.htm
tech.root: security
ms.assetid: a2df73ee-6c95-40d9-b1cb-9eaddb4100d6
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_GSS_INFO, PSECPKG_GSS_INFO, PSECPKG_GSS_INFO structure pointer [Security], SECPKG_GSS_INFO, SECPKG_GSS_INFO structure [Security], _ssp_secpkg_gss_info, ntsecpkg/PSECPKG_GSS_INFO, ntsecpkg/SECPKG_GSS_INFO, security.secpkg_gss_info'
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
req.typenames: SECPKG_GSS_INFO, *PSECPKG_GSS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_GSS_INFO
 - ntsecpkg/_SECPKG_GSS_INFO
 - PSECPKG_GSS_INFO
 - ntsecpkg/PSECPKG_GSS_INFO
 - SECPKG_GSS_INFO
 - ntsecpkg/SECPKG_GSS_INFO
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
 - SECPKG_GSS_INFO
---

# SECPKG_GSS_INFO structure


## -description

A <b>SECPKG_GSS_INFO</b> structure contains information used for GSS-compatible negotiations.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field EncodedIdLength

The encoded GSS OID length.

### -field EncodedId

The encoded GSS OID.