---
UID: NC:ntsecpkg.CrediUnmarshalandDecodeStringFn
title: CrediUnmarshalandDecodeStringFn (ntsecpkg.h)

description: Transforms a marshaled string back into its original form, and decrypts the unmarshaled string.
old-location: security\crediunmarshalanddecodestring.htm
tech.root: SecAuthN
ms.assetid: 15423c8d-ea3b-4981-b059-5828555a9e89

ms.date: 12/05/2018
ms.keywords: CrediUnmarshalandDecodeString, CrediUnmarshalandDecodeString callback function [Security], CrediUnmarshalandDecodeStringFn, CrediUnmarshalandDecodeStringFn callback, ntsecpkg/CrediUnmarshalandDecodeString, security.crediunmarshalanddecodestring
ms.topic: callback
f1_keywords:
- ntsecpkg/CrediUnmarshalandDecodeString
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- CrediUnmarshalandDecodeString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

