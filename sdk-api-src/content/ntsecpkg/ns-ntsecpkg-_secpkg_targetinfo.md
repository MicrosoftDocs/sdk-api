---
UID: NS:ntsecpkg._SECPKG_TARGETINFO
title: "_SECPKG_TARGETINFO"
author: windows-sdk-content
description: Specifies the target of an authentication request.
old-location: security\secpkg_targetinfo.htm
old-project: SecAuthN
ms.assetid: c8d4ac70-743b-42b1-940c-d3d37a6174bc
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSECPKG_TARGETINFO, PSECPKG_TARGETINFO, PSECPKG_TARGETINFO structure pointer [Security], SECPKG_TARGETINFO, SECPKG_TARGETINFO structure [Security], _SECPKG_TARGETINFO, ntsecpkg/PSECPKG_TARGETINFO, ntsecpkg/SECPKG_TARGETINFO, security.secpkg_targetinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SECPKG_TARGETINFO, *PSECPKG_TARGETINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	SECPKG_TARGETINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SECPKG_TARGETINFO structure


## -description


Specifies the target of an authentication request.


## -struct-fields




### -field DomainSid

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that specifies the domain of the target computer.


### -field ComputerName

The name of the target computer.


## -see-also




<a href="https://msdn.microsoft.com/01d1b74a-14d9-40cd-bcca-a031f5fc9cbb">SpValidateTargetInfoFn</a>
 

 

