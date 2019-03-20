---
UID: NS:sspi._SEC_WINNT_AUTH_DATA
title: SEC_WINNT_AUTH_DATA (sspi.h)
author: windows-sdk-content
description: Specifies authentication data.
old-location: security\sec_winnt_auth_data.htm
tech.root: SecAuthN
ms.assetid: d5319273-ef6c-4971-9336-394394d0dbc3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSEC_WINNT_AUTH_DATA, PSEC_WINNT_AUTH_DATA, PSEC_WINNT_AUTH_DATA structure pointer [Security], SEC_WINNT_AUTH_DATA, SEC_WINNT_AUTH_DATA structure [Security], security.sec_winnt_auth_data, sspi/PSEC_WINNT_AUTH_DATA, sspi/SEC_WINNT_AUTH_DATA"
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
 - SEC_WINNT_AUTH_DATA
product: Windows
targetos: Windows
req.typenames: SEC_WINNT_AUTH_DATA, *PSEC_WINNT_AUTH_DATA
req.redist: 
---

# SEC_WINNT_AUTH_DATA structure


## -description


Specifies authentication data.


## -struct-fields




### -field CredType

The type of credential specified by the <b>CredData</b> member


### -field CredData

A structure that specifies the offset from the beginning of this structure and size, in bytes, of the authentication data.


## -see-also




<a href="https://msdn.microsoft.com/ee511497-2b70-4c51-bcc2-7585143b4f43">SEC_WINNT_AUTH_BYTE_VECTOR</a>
 

 

