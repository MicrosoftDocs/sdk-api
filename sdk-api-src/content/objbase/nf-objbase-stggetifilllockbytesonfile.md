---
UID: NF:objbase.StgGetIFillLockBytesOnFile
title: StgGetIFillLockBytesOnFile function (objbase.h)
description: Opens a wrapper object on a temporary file.
helpviewer_keywords: ["StgGetIFillLockBytesOnFile","StgGetIFillLockBytesOnFile function [Structured Storage]","_stg_stggetifilllockbytesonfile","objbase/StgGetIFillLockBytesOnFile","stg.stggetifilllockbytesonfile"]
old-location: stg\stggetifilllockbytesonfile.htm
tech.root: Stg
ms.assetid: 948724ff-d1eb-43ca-b498-6296909cfb28
ms.date: 12/05/2018
ms.keywords: StgGetIFillLockBytesOnFile, StgGetIFillLockBytesOnFile function [Structured Storage], _stg_stggetifilllockbytesonfile, objbase/StgGetIFillLockBytesOnFile, stg.stggetifilllockbytesonfile
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - StgGetIFillLockBytesOnFile
 - objbase/StgGetIFillLockBytesOnFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - StgGetIFillLockBytesOnFile
---

# StgGetIFillLockBytesOnFile function


## -description

<p class="CCE_Message">[The <b>StgGetIFillLockBytesOnFile</b>  function is obsolete. The following information is provided to support versions of Windows prior to Windows 2000.]

The <b>StgGetIFillLockBytesOnFile</b>  function opens a wrapper object on a temporary file.

## -parameters

### -param pwcsName [in]

A pointer to the null-terminated unicode string name of the file for which a wrapper object is created.

### -param ppflb [out]

A pointer to 
<a href="/windows/desktop/api/objidl/nn-objidl-ifilllockbytes">IFillLockBytes</a>* pointer variable that receives the interface pointer to the new byte array wrapper object.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, in addition to the following:

The <b>StgGetIFillLockBytesOnFile</b>  function can also return any file system errors.

## -remarks

The moniker that manages the downloading of the file specified in <i>pwcsName</i> calls this function in the course of creating the asynchronous storage necessary to manage the asynchronous downloading of data. The moniker first creates a temporary file, then calls this function to create the wrapper object on that file. Finally, the moniker calls 
<a href="/windows/desktop/api/objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes">StgOpenAsyncDocfileOnIFillLockBytes</a> to open the root storage of the compound file to be downloaded into the temporary file.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ifilllockbytes">IFillLockBytes</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes">StgOpenAsyncDocfileOnIFillLockBytes</a>