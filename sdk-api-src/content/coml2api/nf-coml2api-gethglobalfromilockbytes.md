---
UID: NF:coml2api.GetHGlobalFromILockBytes
title: GetHGlobalFromILockBytes function (coml2api.h)
description: The GetHGlobalFromILockBytes function retrieves a global memory handle to a byte array object created using the CreateILockBytesOnHGlobal function.
helpviewer_keywords: ["GetHGlobalFromILockBytes","GetHGlobalFromILockBytes function [Structured Storage]","_stg_gethglobalfromilockbytes","coml2api/GetHGlobalFromILockBytes","stg.gethglobalfromilockbytes"]
old-location: stg\gethglobalfromilockbytes.htm
tech.root: Stg
ms.assetid: 084fcd1d-5b85-448c-862a-378353e1e2e6
ms.date: 12/05/2018
ms.keywords: GetHGlobalFromILockBytes, GetHGlobalFromILockBytes function [Structured Storage], _stg_gethglobalfromilockbytes, coml2api/GetHGlobalFromILockBytes, stg.gethglobalfromilockbytes
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetHGlobalFromILockBytes
 - coml2api/GetHGlobalFromILockBytes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - GetHGlobalFromILockBytes
---

# GetHGlobalFromILockBytes function


## -description

The 
<b>GetHGlobalFromILockBytes</b> function retrieves a global memory handle to a byte array object created using the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal">CreateILockBytesOnHGlobal</a> function.

## -parameters

### -param plkbyt [in]

Pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface on the byte-array object previously created by a call to the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal">CreateILockBytesOnHGlobal</a> function.

### -param phglobal [out]

Pointer to the current memory handle used by the specified byte-array object.

## -returns

This function returns HRESULT.

## -remarks

After a call to 
<a href="/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal">CreateILockBytesOnHGlobal</a>, which creates a byte array object on global memory, 
<b>GetHGlobalFromILockBytes</b> retrieves a pointer to the handle of the global memory underlying the byte array object. The handle this function returns might be different from the original handle due to intervening calls to the <a href="/windows/desktop/api/winbase/nf-winbase-globalrealloc">GlobalReAlloc</a> function.

The contents of the returned memory handle can be written to a clean disk file, and then opened as a storage object using the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage">StgOpenStorage</a> function.

This function only works within the same process from which the byte array was created.

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal">CreateILockBytesOnHGlobal</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage">StgOpenStorage</a>