---
UID: NF:msctf.ITfCategoryMgr.RegisterCategory
title: ITfCategoryMgr::RegisterCategory (msctf.h)
description: ITfCategoryMgr::RegisterCategory method
helpviewer_keywords: ["ITfCategoryMgr interface [Text Services Framework]","RegisterCategory method","ITfCategoryMgr.RegisterCategory","ITfCategoryMgr::RegisterCategory","RegisterCategory","RegisterCategory method [Text Services Framework]","RegisterCategory method [Text Services Framework]","ITfCategoryMgr interface","_tsf_itfcategorymgr_registercategory_ref","msctf/ITfCategoryMgr::RegisterCategory","tsf.itfcategorymgr_registercategory"]
old-location: tsf\itfcategorymgr_registercategory.htm
tech.root: TSF
ms.assetid: 9e9a72a8-ea9b-4438-992c-5a7db64f7d82
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterCategory method, ITfCategoryMgr.RegisterCategory, ITfCategoryMgr::RegisterCategory, RegisterCategory, RegisterCategory method [Text Services Framework], RegisterCategory method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registercategory_ref, msctf/ITfCategoryMgr::RegisterCategory, tsf.itfcategorymgr_registercategory
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
 - ITfCategoryMgr::RegisterCategory
 - msctf/ITfCategoryMgr::RegisterCategory
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
 - ITfCategoryMgr.RegisterCategory
---

# ITfCategoryMgr::RegisterCategory


## -description

Adds a specified GUID to the specified category in the Windows registry.

## -parameters

### -param rclsid [in]

Contains the CLSID of the text service that owns the item.

### -param rcatid [in]

Contains a GUID value that identifies the category to register the item under. This can be a user-defined category or one of the <a href="/windows/desktop/TSF/predefined-category-values">predefined category values</a>.

### -param rguid [in]

Contains a GUID value that identifies the item to register.

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
</table>

## -see-also

[ITfCategoryMgr interface](nn-msctf-itfcategorymgr.md), [ITfCategoryMgr::UnregisterCategory](nf-msctf-itfcategorymgr-unregistercategory.md), [Predefined Category Values](/windows/desktop/TSF/predefined-category-values)