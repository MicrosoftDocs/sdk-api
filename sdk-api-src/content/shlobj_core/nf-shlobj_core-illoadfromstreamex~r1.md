---
UID: NF:shlobj_core.ILLoadFromStreamEx~r1
title: ILLoadFromStreamEx
description: The ILLoadFromStreamEx function loads an ITEMIDLIST from an IStream. (ILLoadFromStreamEx r1)
ms.date: 08/02/2022
ms.keywords: ILLoadFromStreamEx
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shlobj_core.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCore.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ILLoadFromStreamEx
 - shlobj_core/ILLoadFromStreamEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - shlobj_core.h
api_name:
 - ILLoadFromStreamEx
---

# ILLoadFromStreamEx function


## -description

<p class="CCE_Message">[<b>ILLoadFromStreamEx(IStream*, PIDLIST_RELATIVE*)</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Loads an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> from an 
    <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -parameters

### -param pstm

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface from which the  
      <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> loads.

### -param ppidl

Type: <b>PIDLIST_RELATIVE*</b>

When this method returns and succeeds, contains the resulting relative 
      <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>. If it fails, contains 
      <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

## -see-also
