---
UID: NC:ntsecpkg.CrediUnmarshalandDecodeStringFn
title: CrediUnmarshalandDecodeStringFn
author: windows-driver-content
description: Transforms a marshaled string back into its original form, and decrypts the unmarshaled string.
old-location: security\crediunmarshalanddecodestring.htm
old-project: SecAuthN
ms.assetid: 15423c8d-ea3b-4981-b059-5828555a9e89
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CrediUnmarshalandDecodeString, CrediUnmarshalandDecodeString function [Security], CrediUnmarshalandDecodeStringFn, ntsecpkg/CrediUnmarshalandDecodeString, security.crediunmarshalanddecodestring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CrediUnmarshalandDecodeString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CrediUnmarshalandDecodeStringFn callback function


## -description


Transforms a marshaled string back into its original form, and decrypts the unmarshaled string.


## -parameters




### -param MarshaledString [in]

The marshaled, encrypted string.


### -param *Blob [out]

A pointer to the unmarshaled, decrypted string.


### -param *BlobSize [out]

A pointer to the size, in bytes, of the buffer pointed to by the <i>Blob</i> parameter.


### -param *IsFailureFatal [out]

A pointer to a <b>BOOLEAN</b> variable to receive a value that indicates whether the caller should complete the operation. If the value of this parameter is <b>TRUE</b>, the caller should not complete the operation.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.




## -remarks



A pointer to the <b>CrediUnmarshalandDecodeString</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

