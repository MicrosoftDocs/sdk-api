---
UID: NS:ntsecpkg._SECPKG_CONTEXT_THUNKS
title: SECPKG_CONTEXT_THUNKS (ntsecpkg.h)
description: The SECPKG_CONTEXT_THUNKS structure contains information about QueryContextAttributes (General) calls to be executed in LSA mode.This structure is used by the SpGetExtendedInformation and SpSetExtendedInformation functions.
helpviewer_keywords: ["*PSECPKG_CONTEXT_THUNKS","PSECPKG_CONTEXT_THUNKS","PSECPKG_CONTEXT_THUNKS structure pointer [Security]","SECPKG_CONTEXT_THUNKS","SECPKG_CONTEXT_THUNKS structure [Security]","_ssp_secpkg_context_thunks","ntsecpkg/PSECPKG_CONTEXT_THUNKS","ntsecpkg/SECPKG_CONTEXT_THUNKS","security.secpkg_context_thunks"]
old-location: security\secpkg_context_thunks.htm
tech.root: security
ms.assetid: 66604eaf-37f1-4c46-a62a-d8c821ad9039
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_CONTEXT_THUNKS, PSECPKG_CONTEXT_THUNKS, PSECPKG_CONTEXT_THUNKS structure pointer [Security], SECPKG_CONTEXT_THUNKS, SECPKG_CONTEXT_THUNKS structure [Security], _ssp_secpkg_context_thunks, ntsecpkg/PSECPKG_CONTEXT_THUNKS, ntsecpkg/SECPKG_CONTEXT_THUNKS, security.secpkg_context_thunks'
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
req.typenames: SECPKG_CONTEXT_THUNKS, *PSECPKG_CONTEXT_THUNKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_CONTEXT_THUNKS
 - ntsecpkg/_SECPKG_CONTEXT_THUNKS
 - PSECPKG_CONTEXT_THUNKS
 - ntsecpkg/PSECPKG_CONTEXT_THUNKS
 - SECPKG_CONTEXT_THUNKS
 - ntsecpkg/SECPKG_CONTEXT_THUNKS
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
 - SECPKG_CONTEXT_THUNKS
---

# SECPKG_CONTEXT_THUNKS structure


## -description

The <b>SECPKG_CONTEXT_THUNKS</b> structure contains information about 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> calls to be executed in LSA mode.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field InfoLevelCount

The number of attributes specified by the <i>Levels</i> parameter.

### -field Levels

An array of one or more context attributes. For a complete list of valid values, see 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>.