---
UID: NS:ntsecpkg._SECPKG_MUTUAL_AUTH_LEVEL
title: "_SECPKG_MUTUAL_AUTH_LEVEL"
author: windows-driver-content
description: The SECPKG_MUTUAL_AUTH_LEVEL structure contains the authentication level used by a security package.
old-location: security\secpkg_mutual_auth_level.htm
old-project: SecAuthN
ms.assetid: f56cd322-8f82-43d7-a666-7067bf23b0a7
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PSECPKG_MUTUAL_AUTH_LEVEL, PSECPKG_MUTUAL_AUTH_LEVEL, PSECPKG_MUTUAL_AUTH_LEVEL structure pointer [Security], SECPKG_MUTUAL_AUTH_LEVEL, SECPKG_MUTUAL_AUTH_LEVEL structure [Security], _SECPKG_MUTUAL_AUTH_LEVEL, _ssp_secpkg_mutual_auth_level, ntsecpkg/PSECPKG_MUTUAL_AUTH_LEVEL, ntsecpkg/SECPKG_MUTUAL_AUTH_LEVEL, security.secpkg_mutual_auth_level"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SECPKG_MUTUAL_AUTH_LEVEL, *PSECPKG_MUTUAL_AUTH_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	SECPKG_MUTUAL_AUTH_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SECPKG_MUTUAL_AUTH_LEVEL structure


## -description


The <b>SECPKG_MUTUAL_AUTH_LEVEL</b> structure contains the authentication level used by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field MutualAuthLevel

The mutual authentication level.

