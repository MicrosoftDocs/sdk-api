---
UID: NF:msctf.ITfCategoryMgr.RegisterGUID
title: ITfCategoryMgr::RegisterGUID (msctf.h)
description: ITfCategoryMgr::RegisterGUID method
helpviewer_keywords: ["ITfCategoryMgr interface [Text Services Framework]","RegisterGUID method","ITfCategoryMgr.RegisterGUID","ITfCategoryMgr::RegisterGUID","RegisterGUID","RegisterGUID method [Text Services Framework]","RegisterGUID method [Text Services Framework]","ITfCategoryMgr interface","_tsf_itfcategorymgr_registerguid_ref","msctf/ITfCategoryMgr::RegisterGUID","tsf.itfcategorymgr_registerguid"]
old-location: tsf\itfcategorymgr_registerguid.htm
tech.root: TSF
ms.assetid: d0de17d9-be3a-4f68-a77d-880047775952
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterGUID method, ITfCategoryMgr.RegisterGUID, ITfCategoryMgr::RegisterGUID, RegisterGUID, RegisterGUID method [Text Services Framework], RegisterGUID method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registerguid_ref, msctf/ITfCategoryMgr::RegisterGUID, tsf.itfcategorymgr_registerguid
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
 - ITfCategoryMgr::RegisterGUID
 - msctf/ITfCategoryMgr::RegisterGUID
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
 - ITfCategoryMgr.RegisterGUID
---

# ITfCategoryMgr::RegisterGUID


## -description

Adds a GUID to the internal table and obtains an atom for the GUID.

## -parameters

### -param rguid [in]

Contains the GUID to obtain the identifier for.

### -param pguidatom [out]

Pointer to a <a href="/windows/desktop/TSF/tfguidatom">TfGuidAtom</a> value that receives the identifier of the GUID.

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
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguidatom</i> is invalid.

</td>
</tr>
</table>

## -remarks

Identical <b>GUID</b> values receive identical <b>TfGuidAtom</b> values.

A <b>TfGuidAtom</b> value is only valid within the process that <b>ITfCategoryMgr::RegisterGUID</b> is called from.

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::GetGUID](nf-msctf-itfcategorymgr-getguid.md), [ITfCategoryMgr::IsEqualTfGuidAtom](nf-msctf-itfcategorymgr-isequaltfguidatom.md), [TfGuidAtom](/windows/win32/tsf/tfguidatom)