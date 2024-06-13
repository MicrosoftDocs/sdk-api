---
UID: NF:ocidl.ISpecifyPropertyPages.GetPages
title: ISpecifyPropertyPages::GetPages (ocidl.h)
description: Retrieves a list of property pages that can be displayed in this object's property sheet.
helpviewer_keywords: ["GetPages","GetPages method [COM]","GetPages method [COM]","ISpecifyPropertyPages interface","ISpecifyPropertyPages interface [COM]","GetPages method","ISpecifyPropertyPages.GetPages","ISpecifyPropertyPages::GetPages","_ctrl_ispecifypropertypages_getpages","com.ispecifypropertypages_getpages","ocidl/ISpecifyPropertyPages::GetPages"]
old-location: com\ispecifypropertypages_getpages.htm
tech.root: com
ms.assetid: 82b652da-b49a-47a7-a959-522b051bfd59
ms.date: 12/05/2018
ms.keywords: GetPages, GetPages method [COM], GetPages method [COM],ISpecifyPropertyPages interface, ISpecifyPropertyPages interface [COM],GetPages method, ISpecifyPropertyPages.GetPages, ISpecifyPropertyPages::GetPages, _ctrl_ispecifypropertypages_getpages, com.ispecifypropertypages_getpages, ocidl/ISpecifyPropertyPages::GetPages
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpecifyPropertyPages::GetPages
 - ocidl/ISpecifyPropertyPages::GetPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - ISpecifyPropertyPages.GetPages
---

## -description

Retrieves a list of property pages that can be displayed in this object's property sheet.

## -parameters

### -param pPages [out]

A pointer to a caller-allocated <a href="/windows/win32/api/ocidl/ns-ocidl-cauuid">CAUUID</a> structure that the function initializes and fills in before it returns. The <b>pElems</b> member in the structure is allocated by the function with <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and should be freed by the caller with <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pPages</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/win32/api/ocidl/ns-ocidl-cauuid">CAUUID</a> structure is caller-allocated, but is not initialized by the caller. The <b>GetPages</b> method fills the <b>cElements</b> member in the structure. This method also allocates memory for the array pointed to by the <b>pElems</b> member using <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Then, it fills the newly allocated array. After this method returns successfully, the structure contains a counted array of UUIDs, each UUID specifying a property page CLSID.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller must release the memory pointed to by the <b>pElems</b> member of <a href="/windows/win32/api/ocidl/ns-ocidl-cauuid">CAUUID</a>, using <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not allowed as a return value, because an object with no property pages should not expose the <a href="/windows/win32/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPages</a> interface.

## -see-also

<a href="/windows/win32/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPages</a>
