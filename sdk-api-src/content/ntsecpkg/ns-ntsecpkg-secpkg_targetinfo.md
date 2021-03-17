---
UID: NS:ntsecpkg._SECPKG_TARGETINFO
title: SECPKG_TARGETINFO (ntsecpkg.h)
description: Specifies the target of an authentication request.
helpviewer_keywords: ["*PSECPKG_TARGETINFO","PSECPKG_TARGETINFO","PSECPKG_TARGETINFO structure pointer [Security]","SECPKG_TARGETINFO","SECPKG_TARGETINFO structure [Security]","ntsecpkg/PSECPKG_TARGETINFO","ntsecpkg/SECPKG_TARGETINFO","security.secpkg_targetinfo"]
old-location: security\secpkg_targetinfo.htm
tech.root: security
ms.assetid: c8d4ac70-743b-42b1-940c-d3d37a6174bc
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_TARGETINFO, PSECPKG_TARGETINFO, PSECPKG_TARGETINFO structure pointer [Security], SECPKG_TARGETINFO, SECPKG_TARGETINFO structure [Security], ntsecpkg/PSECPKG_TARGETINFO, ntsecpkg/SECPKG_TARGETINFO, security.secpkg_targetinfo'
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
req.typenames: SECPKG_TARGETINFO, *PSECPKG_TARGETINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_TARGETINFO
 - ntsecpkg/_SECPKG_TARGETINFO
 - PSECPKG_TARGETINFO
 - ntsecpkg/PSECPKG_TARGETINFO
 - SECPKG_TARGETINFO
 - ntsecpkg/SECPKG_TARGETINFO
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
 - SECPKG_TARGETINFO
---

# SECPKG_TARGETINFO structure


## -description

Specifies the target of an authentication request.

## -struct-fields

### -field DomainSid

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that specifies the domain of the target computer.

### -field ComputerName

The name of the target computer.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spvalidatetargetinfofn">SpValidateTargetInfoFn</a>