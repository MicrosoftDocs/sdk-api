---
UID: NF:coml2api.StgIsStorageILockBytes
title: StgIsStorageILockBytes function (coml2api.h)
description: The StgIsStorageILockBytes function indicates whether the specified byte array contains a storage object.
helpviewer_keywords: ["StgIsStorageILockBytes","StgIsStorageILockBytes function [Structured Storage]","_stg_stgisstorageilockbytes","coml2api/StgIsStorageILockBytes","stg.stgisstorageilockbytes"]
old-location: stg\stgisstorageilockbytes.htm
tech.root: Stg
ms.assetid: ce0e29fd-1b21-4064-8e37-1a5d5df8bb61
ms.date: 12/05/2018
ms.keywords: StgIsStorageILockBytes, StgIsStorageILockBytes function [Structured Storage], _stg_stgisstorageilockbytes, coml2api/StgIsStorageILockBytes, stg.stgisstorageilockbytes
req.header: coml2api.h
req.include-header: Objbase.h
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
 - StgIsStorageILockBytes
 - coml2api/StgIsStorageILockBytes
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
 - StgIsStorageILockBytes
---

# StgIsStorageILockBytes function


## -description

The <b>StgIsStorageILockBytes</b> function indicates whether the specified byte array contains a storage object.

## -parameters

### -param plkbyt

<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> pointer to the byte array to be examined.

## -returns

This function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface error return values. See 
<a href="/windows/desktop/com/error-handling-strategies">Error Handling Strategies</a> and 
<a href="/windows/desktop/com/handling-unknown-errors">Handling Unknown Errors</a>

## -remarks

At the beginning of the byte array underlying a storage object is a signature distinguishing a storage object (supporting the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface) from other file formats. The 
<b>StgIsStorageILockBytes</b> function is useful to applications whose documents use a byte array (a byte array object supports the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface) that might or might not use storage objects.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile">StgIsStorageFile</a>