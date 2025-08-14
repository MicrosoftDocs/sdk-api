---
UID: NF:combaseapi.PropVariantClear
title: PropVariantClear function (combaseapi.h)
description: Frees all elements that can be freed in a given PROPVARIANT structure.
helpviewer_keywords: ["PropVariantClear","PropVariantClear function [Structured Storage]","_stg_propvariantclear","combaseapi/PropVariantClear","stg.propvariantclear"]
old-location: stg\propvariantclear.htm
tech.root: Stg
ms.assetid: 062b6065-a56f-4ecd-b232-3ba338a6d806
ms.date: 12/05/2018
ms.keywords: PropVariantClear, PropVariantClear function [Structured Storage], _stg_propvariantclear, combaseapi/PropVariantClear, stg.propvariantclear
req.header: combaseapi.h
req.include-header: 
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
 - PropVariantClear
 - combaseapi/PropVariantClear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - PropVariantClear
---

# PropVariantClear function


## -description

The <b>PropVariantClear</b> function
			frees all elements that can be freed in a given 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.   For complex elements with known element pointers, the underlying elements are freed prior to freeing the containing element.

## -parameters

### -param pvar [in]

A pointer to an initialized 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure for which any deallocatable elements are to be freed. On return, all zeroes are written to the 
<b>PROPVARIANT</b> structure.

## -returns

This function returns HRESULT.

## -remarks

At any level of indirection, <b>NULL</b> pointers are ignored. For example, the <i>pvar</i> parameter  points to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type <b>VT_CF</b>. The  <b>pclipdata</b> member of the <b>PROPVARIANT</b> structure points to a <b>CLIPDATA</b> structure. The <i>pClipData</i> pointer in the <b>CLIPDATA</b> structure is  <b>NULL</b>.  In this example, the <i>pClipData</i> pointer is ignored.  However, the <b>CLIPDATA</b> structure pointed to by the <b>pclipdata</b> member of the <b>PROPVARIANT</b> structure is freed.

On return, this function writes zeroes to the specified 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure, so the VT-type is <b>VT_EMPTY</b>.

Passing <b>NULL</b> as the <i>pvar</i> parameter produces a return code of S_OK.

<div class="alert"><b>Note</b>  Do not use this function to initialize 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures. Instead, initialize these structures using the 
<a href="/windows/desktop/api/propidl/nf-propidl-propvariantinit">PropVariantInit</a> macro (defined in Propidl.h).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/propidl/nf-propidl-freepropvariantarray">FreePropVariantArray</a>