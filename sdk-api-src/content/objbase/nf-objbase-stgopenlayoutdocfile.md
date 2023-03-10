---
UID: NF:objbase.StgOpenLayoutDocfile
title: StgOpenLayoutDocfile function (objbase.h)
description: Opens a compound file on an ILockBytes implementation that is capable of monitoring sector data.
helpviewer_keywords: ["StgOpenLayoutDocfile","StgOpenLayoutDocfile function [Structured Storage]","_stg_stgopenlayoutdocfile","objbase/StgOpenLayoutDocfile","stg.stgopenlayoutdocfile"]
old-location: stg\stgopenlayoutdocfile.htm
tech.root: Stg
ms.assetid: 6ecfb6bd-e623-42b6-9b95-f0563921ac15
ms.date: 12/05/2018
ms.keywords: StgOpenLayoutDocfile, StgOpenLayoutDocfile function [Structured Storage], _stg_stgopenlayoutdocfile, objbase/StgOpenLayoutDocfile, stg.stgopenlayoutdocfile
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
req.lib: DfLayout.lib
req.dll: DfLayout.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StgOpenLayoutDocfile
 - objbase/StgOpenLayoutDocfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DfLayout.dll
api_name:
 - StgOpenLayoutDocfile
---

# StgOpenLayoutDocfile function


## -description

Not supported.

The <b>StgOpenLayoutDocfile</b> function opens a compound file on an 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> implementation that is capable of monitoring sector data. To call  <b>StgOpenLayoutDocfile</b>, both  DfLayout.dll and DfLayout.lib are required.


<div class="alert"><b>Note</b>  Do not use this function. Use the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-copyto">IStorage::CopyTo</a>  
 method instead. <b>CopyTo</b> can be used to layout a docfile, thus improving performance in most scenarios.</div>
<div> </div>

## -parameters

### -param pwcsDfName [in]

A pointer to the null-terminated Unicode string name of the compound file to be opened.

### -param grfMode [in]

Access mode to use when opening the newly created storage object. Values are taken from the 
<a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. Be aware that priority mode and exclusions are not supported. The most common access mode is likely to be STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE.

### -param reserved [in]

Reserved for future use.

### -param ppstgOpen [out]

A pointer to 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer variable that receives the interface pointer to the root object of the newly created root storage object.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, in addition to the following:

The <b>StgOpenLayoutDocfile</b> function can also return any of the error values returned by the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes">StgOpenStorageOnILockBytes</a> function.

## -remarks

The compound file implementation created by this function exposes the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilayoutstorage">ILayoutStorage</a> interface on its root storage. Applications use this interface to express the optimal layout of their compound files in order to download and render data more rapidly over a slow link. 
<b>StgOpenLayoutDocfile</b> returns a pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the root storage of the newly created compound file. Using this pointer, applications call <b>QueryInterface</b> to obtain a pointer to 
<b>ILayoutStorage</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-copyto">CopyTo</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>