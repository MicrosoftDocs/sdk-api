---
UID: NF:shlobj_core.ILLoadFromStreamEx~r2
title: ILLoadFromStreamEx
ms.date: 01/30/19
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
f1_keywords:
 - ILLoadFromStreamEx
 - shlobj_core/ILLoadFromStreamEx
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - 
api_location:
 - shlobj_core.h
api_name:
 - ILLoadFromStreamEx
---

# ILLoadFromStreamEx function


## -description

<p class="CCE_Message">[<b>ILLoadFromStreamEx(IStream*, PITEMID_CHILD*)</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Loads a child pointer to an item identifier list (PIDL) from an 
    <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -parameters

### -param pstm

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface from which the child PIDL loads.

### -param ppidl

Type: <b>PITEMID_CHILD*</b>

When this function returns and succeeds, contains a child PIDL, which contains exactly one <b>SHITEMID</b> structure. If it fails, contains <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

For use where STRICT_TYPED_ITEMIDS is defined.

## -see-also