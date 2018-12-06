---
UID: NE:ntsecpkg._SECPKG_NAME_TYPE
title: "_SECPKG_NAME_TYPE"
author: windows-sdk-content
description: The SECPKG_NAME_TYPE enumeration is used to describe the type of name specified for an account.The SECPKG_NAME_TYPE enumeration is used by the GetAuthDataForUser and OpenSamUser functions.
old-location: security\secpkg_name_type.htm
tech.root: secauthn
ms.assetid: 6a534bfa-83ec-408d-ad21-e230a7adc61e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SECPKG_NAME_TYPE, SECPKG_NAME_TYPE enumeration [Security], SecNameAlternateId, SecNameDN, SecNameFlat, SecNameSamCompatible, _SECPKG_NAME_TYPE, _ssp_secpkg_name_type, ntsecpkg/SECPKG_NAME_TYPE, ntsecpkg/SecNameAlternateId, ntsecpkg/SecNameDN, ntsecpkg/SecNameFlat, ntsecpkg/SecNameSamCompatible, security.secpkg_name_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - SECPKG_NAME_TYPE
product: Windows
targetos: Windows
req.typenames: SECPKG_NAME_TYPE
req.redist: 
---

# _SECPKG_NAME_TYPE enumeration


## -description


The <b>SECPKG_NAME_TYPE</b> enumeration is used to describe the type of name specified for an account.

The <b>SECPKG_NAME_TYPE</b> enumeration is used by the 
<a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a> and 
<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a> functions.


## -enum-fields




### -field SecNameSamCompatible

The account name is compatible with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM). An example of a name in SAM-compatible format is <b>"</b><i>ExampleDomain</i><b>\</b><i>UserName</i><b>"</b>.


### -field SecNameAlternateId

The account name is in the AltSecId property of the SAM account.


### -field SecNameFlat

The account name is a flat user principal name (UPN) style account name.


### -field SecNameDN

The account name is the distinguished name of the object.


### -field SecNameSPN



