---
UID: NS:sspi._SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX
title: "_SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX"
author: windows-sdk-content
description: Specifies serialized credentials and a list of security packages that support the credentials.
old-location: security\sec_winnt_auth_packed_credentials_ex.htm
old-project: secauthn
ms.assetid: 33e42e35-e34c-4e89-90c7-8aee5176ae1b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, PSEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, PSEC_WINNT_AUTH_PACKED_CREDENTIALS_EX structure pointer [Security], SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX structure [Security], _SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, security.sec_winnt_auth_packed_credentials_ex, sspi/PSEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, sspi/SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX, *PSEC_WINNT_AUTH_PACKED_CREDENTIALS_EX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX structure


## -description


Specifies serialized credentials and a list of security packages that support the credentials.


## -struct-fields




### -field cbHeaderLength

The size, in bytes, of the structure header.


### -field Flags

This member is reserved. Do not use it.


### -field PackedCredentials

The offset and size of the serialized credentials in this structure.


### -field PackageList

The offset and size of the list of security packages in this structure.

