---
UID: NF:msctf.ITfCategoryMgr.GetGUIDDWORD
title: ITfCategoryMgr::GetGUIDDWORD (msctf.h)
description: ITfCategoryMgr::GetGUIDDWORD method
helpviewer_keywords: ["GetGUIDDWORD","GetGUIDDWORD method [Text Services Framework]","GetGUIDDWORD method [Text Services Framework]","ITfCategoryMgr interface","ITfCategoryMgr interface [Text Services Framework]","GetGUIDDWORD method","ITfCategoryMgr.GetGUIDDWORD","ITfCategoryMgr::GetGUIDDWORD","_tsf_itfcategorymgr_getguiddword_ref","msctf/ITfCategoryMgr::GetGUIDDWORD","tsf.itfcategorymgr_getguiddword"]
old-location: tsf\itfcategorymgr_getguiddword.htm
tech.root: TSF
ms.assetid: 016d77b5-fc08-4d2b-a9c4-50ae7926a057
ms.date: 12/05/2018
ms.keywords: GetGUIDDWORD, GetGUIDDWORD method [Text Services Framework], GetGUIDDWORD method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],GetGUIDDWORD method, ITfCategoryMgr.GetGUIDDWORD, ITfCategoryMgr::GetGUIDDWORD, _tsf_itfcategorymgr_getguiddword_ref, msctf/ITfCategoryMgr::GetGUIDDWORD, tsf.itfcategorymgr_getguiddword
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
 - ITfCategoryMgr::GetGUIDDWORD
 - msctf/ITfCategoryMgr::GetGUIDDWORD
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
 - ITfCategoryMgr.GetGUIDDWORD
---

# ITfCategoryMgr::GetGUIDDWORD


## -description

Obtains the DWORD value of the specified GUID from the Windows registry.

## -parameters

### -param rguid [in]

Specifies the address of the GUID for which to get the value.

### -param pdw [out]

Pointer to the <b>DWORD</b> variable that receives the value of the GUID.

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
The method was unable to get the <b>DWORD</b> value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pdw</i> parameter was <b>NULL</b> on input.

</td>
</tr>
</table>

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::RegisterGUIDDWORD](nf-msctf-itfcategorymgr-registerguiddword.md), [ITfCategoryMgr::UnregisterGUIDDWORD](nf-msctf-itfcategorymgr-unregisterguiddword.md)

