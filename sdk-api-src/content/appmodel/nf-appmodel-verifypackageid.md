---
UID: NF:appmodel.VerifyPackageId
title: VerifyPackageId
description: Verifies whether or not a package id is syntactically valid.
ms.date: 01/24/2025
tech.root: appxpkg
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appmodel.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - api-ms-win-appmodel-runtime-l1-1-2.dll
 - api-ms-win-appmodel-runtime-l1-1-1.dll
 - appmodel.h
api_name:
 - VerifyPackageId
f1_keywords:
 - VerifyPackageId
 - appmodel/VerifyPackageId
dev_langs:
 - c++
helpviewer_keywords:
 - VerifyPackageId
---

## -description

Verifies whether or not a package id is syntactically valid.

## -parameters

### -param packageId

Type: \_In\_ **const [PACKAGE_ID](/windows/win32/api/appmodel/ns-appmodel-package_id)\***

The package id to verify.

## -returns

Type: **LONG**

Returns **ERROR_SUCCESS** if the input is syntactically valid; otherwise **ERROR_INVALID_PARAMETER**.

## -remarks

## -see-also
