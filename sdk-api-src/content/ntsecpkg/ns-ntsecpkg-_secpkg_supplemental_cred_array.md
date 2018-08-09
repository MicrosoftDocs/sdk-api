---
UID: NS:ntsecpkg._SECPKG_SUPPLEMENTAL_CRED_ARRAY
title: "_SECPKG_SUPPLEMENTAL_CRED_ARRAY"
author: windows-sdk-content
description: The SECPKG_SUPPLEMENTAL_CRED_ARRAY structure contains supplemental credentials information. This structure is used by the LsaApLogonUserEx2 and UpdateCredentials functions.
old-location: security\secpkg_supplemental_cred_array.htm
old-project: secauthn
ms.assetid: b9514e26-29a5-4ba8-a375-1723c0a1ce39
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSECPKG_SUPPLEMENTAL_CRED_ARRAY, PSECPKG_SUPPLEMENTAL_CRED_ARRAY, PSECPKG_SUPPLEMENTAL_CRED_ARRAY structure pointer [Security], SECPKG_SUPPLEMENTAL_CRED_ARRAY, SECPKG_SUPPLEMENTAL_CRED_ARRAY structure [Security], _SECPKG_SUPPLEMENTAL_CRED_ARRAY, _ssp_secpkg_supplemental_cred_array, ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED_ARRAY, ntsecpkg/SECPKG_SUPPLEMENTAL_CRED_ARRAY, security.secpkg_supplemental_cred_array"
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
req.typenames: SECPKG_SUPPLEMENTAL_CRED_ARRAY, *PSECPKG_SUPPLEMENTAL_CRED_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_SUPPLEMENTAL_CRED_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SECPKG_SUPPLEMENTAL_CRED_ARRAY structure


## -description


The <b>SECPKG_SUPPLEMENTAL_CRED_ARRAY</b> structure contains <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> information. This structure is used by the 
<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a> and 
<a href="https://msdn.microsoft.com/952ed682-775a-4370-8a89-15ca35553667">UpdateCredentials</a> functions.


## -struct-fields




### -field CredentialCount

The number of supplemental credentials in the <b>Credentials</b> member.


### -field Credentials.size_is

 


### -field Credentials.size_is.CredentialCount

 


### -field Credentials

An array containing supplemental credentials.

