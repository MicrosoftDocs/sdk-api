---
UID: NS:ntsecpkg._SECPKG_GSS_INFO
title: "_SECPKG_GSS_INFO"
author: windows-sdk-content
description: A SECPKG_GSS_INFO structure contains information used for GSS-compatible negotiations.
old-location: security\secpkg_gss_info.htm
tech.root: secauthn
ms.assetid: a2df73ee-6c95-40d9-b1cb-9eaddb4100d6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PSECPKG_GSS_INFO, PSECPKG_GSS_INFO, PSECPKG_GSS_INFO structure pointer [Security], SECPKG_GSS_INFO, SECPKG_GSS_INFO structure [Security], _SECPKG_GSS_INFO, _ssp_secpkg_gss_info, ntsecpkg/PSECPKG_GSS_INFO, ntsecpkg/SECPKG_GSS_INFO, security.secpkg_gss_info"
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
 - SECPKG_GSS_INFO
product: Windows
targetos: Windows
req.typenames: SECPKG_GSS_INFO, *PSECPKG_GSS_INFO
req.redist: 
---

# _SECPKG_GSS_INFO structure


## -description


A <b>SECPKG_GSS_INFO</b> structure contains information used for GSS-compatible negotiations.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field EncodedIdLength

The encoded GSS OID length.


### -field EncodedId

The encoded GSS OID.

