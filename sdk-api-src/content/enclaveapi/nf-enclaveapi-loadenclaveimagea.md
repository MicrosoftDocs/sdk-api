---
UID: NF:enclaveapi.LoadEnclaveImageA
tech.root: base 
title: LoadEnclaveImageA
ms.date: 07/02/2024
targetos: Windows
description: Loads an image and all of its imports into an enclave. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll; Api-ms-win-core-enclave-l1-1-0.dll 
req.header: enclaveapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only] 
req.target-min-winversvr: Windows Server 2016 [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - LoadEnclaveImageA
 - LoadEnclaveImage
f1_keywords:
 - LoadEnclaveImageA
 - enclaveapi/LoadEnclaveImageA
 - LoadEnclaveImage
 - enclaveapi/LoadEnclaveImage
dev_langs:
 - c++
---

# LoadEnclaveImageA function

## -description

Loads an image and all of its imports into an enclave.

## -parameters

### -param lpEnclaveAddress [in]

The base address of the image into which to load the image.

### -param lpImageName [in]

A NULL-terminated string that contains the name of the image to load.

## -returns

`TRUE` if the function succeeds; otherwise `FALSE`.  

To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

**LoadEnclaveImage** is only supported enclaves that have the **ENCLAVE_TYPE_VBS** enclave type.

You cannot load an image into the enclave after it has been initialized with [InitializeEnclave](nf-enclaveapi-initializeenclave.md).

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[CreateEnclave](nf-enclaveapi-createenclave.md)

[InitializeEnclave](nf-enclaveapi-initializeenclave.md)
