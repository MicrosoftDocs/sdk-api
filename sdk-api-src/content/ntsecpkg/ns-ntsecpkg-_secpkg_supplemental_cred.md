---
UID: NS:ntsecpkg._SECPKG_SUPPLEMENTAL_CRED
title: "_SECPKG_SUPPLEMENTAL_CRED"
author: windows-sdk-content
description: The SECPKG_SUPPLEMENTAL_CRED structure contains supplemental credentials recognized by the security package.
old-location: security\secpkg_supplemental_cred.htm
tech.root: SecAuthN
ms.assetid: d5a1a986-5343-420d-8553-f1078bbd0e00
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PSECPKG_SUPPLEMENTAL_CRED, PSECPKG_SUPPLEMENTAL_CRED, PSECPKG_SUPPLEMENTAL_CRED structure pointer [Security], SECPKG_SUPPLEMENTAL_CRED, SECPKG_SUPPLEMENTAL_CRED structure [Security], _SECPKG_SUPPLEMENTAL_CRED, _ssp_secpkg_supplemental_cred, ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED, ntsecpkg/SECPKG_SUPPLEMENTAL_CRED, security.secpkg_supplemental_cred"
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
 - SECPKG_SUPPLEMENTAL_CRED
product: Windows
targetos: Windows
req.typenames: SECPKG_SUPPLEMENTAL_CRED, *PSECPKG_SUPPLEMENTAL_CRED
req.redist: 
---

# _SECPKG_SUPPLEMENTAL_CRED structure


## -description


The <b>SECPKG_SUPPLEMENTAL_CRED</b> structure contains <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> recognized by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

The structure is used by the 
<a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a> function and the 
<a href="https://msdn.microsoft.com/b9514e26-29a5-4ba8-a375-1723c0a1ce39">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> structure.


## -struct-fields




### -field PackageName

The name of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> that authenticated the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a>.


### -field CredentialSize

The size of the <b>Credentials</b> member, in bytes.


### -field Credentials

Pointer to a set of package-specific supplemental credentials.


### -field Credentials.size_is

 


### -field Credentials.size_is.CredentialSize

 



