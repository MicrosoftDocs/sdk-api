---
UID: NF:msctf.ITfCategoryMgr.UnregisterGUIDDescription
title: ITfCategoryMgr::UnregisterGUIDDescription (msctf.h)
description: ITfCategoryMgr::UnregisterGUIDDescription method
helpviewer_keywords: ["ITfCategoryMgr interface [Text Services Framework]","UnregisterGUIDDescription method","ITfCategoryMgr.UnregisterGUIDDescription","ITfCategoryMgr::UnregisterGUIDDescription","UnregisterGUIDDescription","UnregisterGUIDDescription method [Text Services Framework]","UnregisterGUIDDescription method [Text Services Framework]","ITfCategoryMgr interface","_tsf_itfcategorymgr_unregisterguiddescription_ref","msctf/ITfCategoryMgr::UnregisterGUIDDescription","tsf.itfcategorymgr_unregisterguiddescription"]
old-location: tsf\itfcategorymgr_unregisterguiddescription.htm
tech.root: TSF
ms.assetid: 42bc1ddc-9f11-40dc-849c-2effc6efe1c8
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],UnregisterGUIDDescription method, ITfCategoryMgr.UnregisterGUIDDescription, ITfCategoryMgr::UnregisterGUIDDescription, UnregisterGUIDDescription, UnregisterGUIDDescription method [Text Services Framework], UnregisterGUIDDescription method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_unregisterguiddescription_ref, msctf/ITfCategoryMgr::UnregisterGUIDDescription, tsf.itfcategorymgr_unregisterguiddescription
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
 - ITfCategoryMgr::UnregisterGUIDDescription
 - msctf/ITfCategoryMgr::UnregisterGUIDDescription
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
 - ITfCategoryMgr.UnregisterGUIDDescription
---

# ITfCategoryMgr::UnregisterGUIDDescription


## -description

Removes the description for a GUID from the Windows registry.

## -parameters

### -param rclsid [in]

Contains the CLSID of the text service that owns the GUID.

### -param rguid [in]

Contains the GUID that the description is removed for.

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
The GUID cannot be found.

</td>
</tr>
</table>

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::GetGUIDDescription](nf-msctf-itfcategorymgr-getguiddescription.md), [ITfCategoryMgr::RegisterGUIDDescription](nf-msctf-itfcategorymgr-registerguiddescription.md)

