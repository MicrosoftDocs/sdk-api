---
UID: NF:roerrorapi.RoGetMatchingRestrictedErrorInfo
tech.root: WinRT
title: RoGetMatchingRestrictedErrorInfo
ms.date: 02/09/2023
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: roerrorapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoGetMatchingRestrictedErrorInfo
f1_keywords:
 - RoGetMatchingRestrictedErrorInfo
 - roerrorapi/RoGetMatchingRestrictedErrorInfo
dev_langs:
 - c++
helpviewer_keywords:
 - RoGetMatchingRestrictedErrorInfo
---

## -description

Retrieves the restricted error information for the specified HRESULT.

## -parameters

### -param hrIn

An HRESULT representing the error for which restricted error info is retrieved.

### -param ppRestrictedErrorInfo

Receives an instance of [IRestrictedErrorInfo](../restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo.md) representing the details of an error, including restricted error information.

## -returns

Returns S_OK on success.

## -remarks

The function checks to see if current error info matches the *hrIn* value passed in and, if not, it originates a matching error info.

## -see-also

