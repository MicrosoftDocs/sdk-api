---
UID: NF:enclaveapi.LoadEnclaveImageW
title: LoadEnclaveImageW function (enclaveapi.h)
description: Loads an image and all of its imports into an enclave. (Unicode)
helpviewer_keywords: ["LoadEnclaveIUmageA", "LoadEnclaveImage", "LoadEnclaveImage function", "LoadEnclaveImageW", "base.loadenclaveimage", "enclaveapi/LoadEnclaveIUmageA", "enclaveapi/LoadEnclaveImage", "enclaveapi/LoadEnclaveImageW"]
old-location: base\loadenclaveimage.htm
tech.root: base
ms.assetid: BC3F3EB4-BB5E-40D6-B877-50694576FA1B
ms.date: 07/02/2024
ms.keywords: LoadEnclaveIUmageA, LoadEnclaveImage, LoadEnclaveImage function, LoadEnclaveImageW, base.loadenclaveimage, enclaveapi/LoadEnclaveIUmageA, enclaveapi/LoadEnclaveImage, enclaveapi/LoadEnclaveImageW
req.header: enclaveapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadEnclaveImageW (Unicode) and LoadEnclaveIUmageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: kernel32.dll; Api-ms-win-core-enclave-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadEnclaveImageW
 - enclaveapi/LoadEnclaveImageW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-enclave-l1-1-1.dll
 - kernel32.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - LoadEnclaveImage
 - LoadEnclaveIUmageA
 - LoadEnclaveImageW
---

# LoadEnclaveImageW function

## -description

Loads an image and all of its imports into an enclave.

## -parameters

### -param lpEnclaveAddress [in]

The base address of the image into which to load the image.

### -param lpImageName [in]

A NULL-terminated string that contains the name of the image to load.

## -returns

`TRUE` if the function succeeds; otherwise `FALSE`. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

**LoadEnclaveImage** is only supported enclaves that have the **ENCLAVE_TYPE_VBS** enclave type.

You cannot load an image into the enclave after it has been initialized with [InitializeEnclave](nf-enclaveapi-initializeenclave.md).

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[CreateEnclave](nf-enclaveapi-createenclave.md)

[InitializeEnclave](nf-enclaveapi-initializeenclave.md)
