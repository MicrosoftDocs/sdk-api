---
UID: NS:ntsecpkg._SECPKG_NEGO2_INFO
title: "_SECPKG_NEGO2_INFO"
author: windows-driver-content
description: Contains extended package information used for NEGO2 negotiations.
old-location: security\secpkg_nego2_info.htm
old-project: SecAuthN
ms.assetid: 8B093B74-DBF2-4DBD-9FDC-72FD6CC3CCA6
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PSECPKG_NEGO2_INFO, PSECPKG_NEGO2_INFO, PSECPKG_NEGO2_INFO structure pointer [Security], SECPKG_NEGO2_INFO, SECPKG_NEGO2_INFO structure [Security], _SECPKG_NEGO2_INFO, ntsecpkg/PSECPKG_NEGO2_INFO, ntsecpkg/SECPKG_NEGO2_INFO, security.secpkg_nego2_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecpkg.h
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
req.typenames: SECPKG_NEGO2_INFO, *PSECPKG_NEGO2_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	SECPKG_NEGO2_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SECPKG_NEGO2_INFO structure


## -description


The <b>SECPKG_NEGO2_INFO</b> structure  contains extended package information used for NEGO2 negotiations.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field AuthScheme

The authentication identifier.


### -field PackageFlags

The flags associated with the authentication package.

