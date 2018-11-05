---
UID: NS:sspi._SEC_WINNT_AUTH_CERTIFICATE_DATA
title: "_SEC_WINNT_AUTH_CERTIFICATE_DATA"
author: windows-sdk-content
description: Specifies serialized certificate information.
old-location: security\sec_winnt_auth_certificate_data.htm
tech.root: secauthn
ms.assetid: 08dc5062-2925-4ec2-aef3-c7ff1cba9544
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PSEC_WINNT_AUTH_CERTIFICATE_DATA, PSEC_WINNT_AUTH_CERTIFICATE_DATA, PSEC_WINNT_AUTH_CERTIFICATE_DATA structure pointer [Security], SEC_WINNT_AUTH_CERTIFICATE_DATA, SEC_WINNT_AUTH_CERTIFICATE_DATA structure [Security], _SEC_WINNT_AUTH_CERTIFICATE_DATA, security.sec_winnt_auth_certificate_data, sspi/PSEC_WINNT_AUTH_CERTIFICATE_DATA, sspi/SEC_WINNT_AUTH_CERTIFICATE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_AUTH_CERTIFICATE_DATA
product: Windows
targetos: Windows
req.typenames: SEC_WINNT_AUTH_CERTIFICATE_DATA, *PSEC_WINNT_AUTH_CERTIFICATE_DATA
req.redist: 
---

# _SEC_WINNT_AUTH_CERTIFICATE_DATA structure


## -description


Specifies serialized certificate information.


## -struct-fields




### -field cbHeaderLength

The size, in bytes,  of the structure header.


### -field cbStructureLength

The size, in bytes, of the certificate information.


### -field Certificate

A structure that specifies the offset from the beginning of this structure and the size, in bytes, of the certificate data.


## -see-also




<a href="https://msdn.microsoft.com/ee511497-2b70-4c51-bcc2-7585143b4f43">SEC_WINNT_AUTH_BYTE_VECTOR</a>
 

 

