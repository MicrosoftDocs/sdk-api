---
UID: NS:ntsecpkg._SECPKG_TARGETINFO
title: SECPKG_TARGETINFO (ntsecpkg.h)
author: windows-sdk-content
description: Specifies the target of an authentication request.
old-location: security\secpkg_targetinfo.htm
tech.root: SecAuthN
ms.assetid: c8d4ac70-743b-42b1-940c-d3d37a6174bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_TARGETINFO, PSECPKG_TARGETINFO, PSECPKG_TARGETINFO structure pointer [Security], SECPKG_TARGETINFO, SECPKG_TARGETINFO structure [Security], ntsecpkg/PSECPKG_TARGETINFO, ntsecpkg/SECPKG_TARGETINFO, security.secpkg_targetinfo'
ms.topic: struct
f1_keywords:
- ntsecpkg/SECPKG_TARGETINFO
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntsecpkg.h
api_name:
- SECPKG_TARGETINFO
targetos: Windows
req.typenames: SECPKG_TARGETINFO, *PSECPKG_TARGETINFO
req.redist: 
ms.custom: 19H1
---

# SECPKG_TARGETINFO structure


## -description


Specifies the target of an authentication request.


## -struct-fields




### -field DomainSid

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that specifies the domain of the target computer.


### -field ComputerName

The name of the target computer.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spvalidatetargetinfofn">SpValidateTargetInfoFn</a>
 

 

