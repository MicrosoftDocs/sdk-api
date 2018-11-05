---
UID: NS:ntsecpkg._SECPKG_EXTRA_OIDS
title: "_SECPKG_EXTRA_OIDS"
author: windows-sdk-content
description: Contains the object identifiers (OIDs) for the extended security package.
old-location: security\secpkg_extra_oids.htm
tech.root: secauthn
ms.assetid: 188EB248-F056-40F4-8A27-6BEC75F14154
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PSECPKG_EXTRA_OIDS, PSECPKG_EXTRA_OIDS, PSECPKG_EXTRA_OIDS structure pointer [Security], SECPKG_EXTRA_OIDS, SECPKG_EXTRA_OIDS structure [Security], _SECPKG_EXTRA_OIDS, ntsecpkg/PSECPKG_EXTRA_OIDS, ntsecpkg/SECPKG_EXTRA_OIDS, security.secpkg_extra_oids"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - SECPKG_EXTRA_OIDS
product: Windows
targetos: Windows
req.typenames: SECPKG_EXTRA_OIDS, *PSECPKG_EXTRA_OIDS
req.redist: 
---

# _SECPKG_EXTRA_OIDS structure


## -description


The <b>SECPKG_EXTRA_OIDS</b> structure contains the object identifiers (OIDs) for the extended security package.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field OidCount

The total number of OIDs in the security package.


### -field Oids

A <a href="https://msdn.microsoft.com/54CF931B-AD1F-4370-A2AF-5DF4BC9EA007">SECPKG_SERIALIZED_OID</a> structure containing the OID data.

