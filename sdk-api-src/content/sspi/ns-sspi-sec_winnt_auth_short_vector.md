---
UID: NS:sspi._SEC_WINNT_AUTH_SHORT_VECTOR
title: SEC_WINNT_AUTH_SHORT_VECTOR
author: windows-sdk-content
description: Specifies the offset and number of characters in an array of USHORT values.
old-location: security\sec_winnt_auth_short_vector.htm
tech.root: secauthn
ms.assetid: c3c1ade7-db2b-4450-97c1-5b67e4ebdcb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSEC_WINNT_AUTH_SHORT_VECTOR, PSEC_WINNT_AUTH_SHORT_VECTOR, PSEC_WINNT_AUTH_SHORT_VECTOR structure pointer [Security], SEC_WINNT_AUTH_SHORT_VECTOR, SEC_WINNT_AUTH_SHORT_VECTOR structure [Security], security.sec_winnt_auth_short_vector, sspi/PSEC_WINNT_AUTH_SHORT_VECTOR, sspi/SEC_WINNT_AUTH_SHORT_VECTOR"
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
 - SEC_WINNT_AUTH_SHORT_VECTOR
product: Windows
targetos: Windows
req.typenames: SEC_WINNT_AUTH_SHORT_VECTOR, *PSEC_WINNT_AUTH_SHORT_VECTOR
req.redist: 
---

# SEC_WINNT_AUTH_SHORT_VECTOR structure


## -description


Specifies the offset and number of characters in an array of <b>USHORT</b> values.


## -struct-fields




### -field ShortArrayOffset

The number of characters before the beginning of the data in a <a href="https://msdn.microsoft.com/33e42e35-e34c-4e89-90c7-8aee5176ae1b">SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX</a> structure.


### -field ShortArrayCount

The  number of characters in the array.

