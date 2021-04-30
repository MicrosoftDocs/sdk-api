---
UID: NF:oleauto.SafeArrayDestroyData
title: SafeArrayDestroyData function (oleauto.h)
description: Destroys all the data in the specified safe array.
helpviewer_keywords: ["SafeArrayDestroyData","SafeArrayDestroyData function [Automation]","_oa96_SafeArrayDestroyData","automat.safearraydestroydata","oleauto/SafeArrayDestroyData"]
old-location: automat\safearraydestroydata.htm
tech.root: automat
ms.assetid: aa9c62ba-79b5-4fcf-b3ed-664016486dfc
ms.date: 12/05/2018
ms.keywords: SafeArrayDestroyData, SafeArrayDestroyData function [Automation], _oa96_SafeArrayDestroyData, automat.safearraydestroydata, oleauto/SafeArrayDestroyData
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayDestroyData
 - oleauto/SafeArrayDestroyData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayDestroyData
---

# SafeArrayDestroyData function


## -description

Destroys all the data in the specified safe array.

## -parameters

### -param psa [in]

A safe array descriptor.

## -returns

This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The array is locked.

</td>
</tr>
</table>

## -remarks

This function is typically used when freeing safe arrays that contain elements with data types other than variants. If objects are stored in the array, Release is called on each object in the array. Safe arrays of variant will have the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> function called on each member and safe arrays of BSTR will have the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function called on each element. <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordclear">IRecordInfo::RecordClear</a> will be called to release object references and other values of a record without deallocating the record.