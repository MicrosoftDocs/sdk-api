---
UID: NF:msctf.ITfCategoryMgr.GetGUIDDescription
title: ITfCategoryMgr::GetGUIDDescription (msctf.h)
description: ITfCategoryMgr::GetGUIDDescription method
helpviewer_keywords: ["GetGUIDDescription","GetGUIDDescription method [Text Services Framework]","GetGUIDDescription method [Text Services Framework]","ITfCategoryMgr interface","ITfCategoryMgr interface [Text Services Framework]","GetGUIDDescription method","ITfCategoryMgr.GetGUIDDescription","ITfCategoryMgr::GetGUIDDescription","_tsf_itfcategorymgr_getguiddescription_ref","msctf/ITfCategoryMgr::GetGUIDDescription","tsf.itfcategorymgr_getguiddescription"]
old-location: tsf\itfcategorymgr_getguiddescription.htm
tech.root: TSF
ms.assetid: e0c4f64e-7e20-4dff-b597-acc280aebf32
ms.date: 12/05/2018
ms.keywords: GetGUIDDescription, GetGUIDDescription method [Text Services Framework], GetGUIDDescription method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],GetGUIDDescription method, ITfCategoryMgr.GetGUIDDescription, ITfCategoryMgr::GetGUIDDescription, _tsf_itfcategorymgr_getguiddescription_ref, msctf/ITfCategoryMgr::GetGUIDDescription, tsf.itfcategorymgr_getguiddescription
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCategoryMgr::GetGUIDDescription
 - msctf/ITfCategoryMgr::GetGUIDDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCategoryMgr.GetGUIDDescription
---

# ITfCategoryMgr::GetGUIDDescription


## -description

Obtains the description of the specified GUID from the Windows registry.

## -parameters

### -param rguid [in]

Specifies the GUID to obtain the description for.

### -param pbstrDesc [out]

Pointer to a <b>BSTR</b> value that receives the description string. Allocate using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The caller must free this memory using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

Pointer to a <b>BSTR</b> value that receives the description string. This must be allocated using <b>SysAllocString</b>. The caller must free this memory using <b>SysFreeString</b> when it is no longer required.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method cannot obtain the description.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstrDesc</i> is invalid.

</td>
</tr>
</table>

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::RegisterGUIDDescription](nf-msctf-itfcategorymgr-registerguiddescription.md), [ITfCategoryMgr::UnregisterGUIDDescription](nf-msctf-itfcategorymgr-unregisterguiddescription.md)