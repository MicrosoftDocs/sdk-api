---
UID: NF:oleauto.SafeArraySetRecordInfo
title: SafeArraySetRecordInfo function (oleauto.h)
description: Sets the record info in the specified safe array.
helpviewer_keywords: ["SafeArraySetRecordInfo","SafeArraySetRecordInfo function [Automation]","_oa96_SafeArraySetRecordInfo","automat.safearraysetrecordinfo","oleauto/SafeArraySetRecordInfo"]
old-location: automat\safearraysetrecordinfo.htm
tech.root: automat
ms.assetid: 85317e8e-7625-4799-9c34-73245f164f85
ms.date: 12/05/2018
ms.keywords: SafeArraySetRecordInfo, SafeArraySetRecordInfo function [Automation], _oa96_SafeArraySetRecordInfo, automat.safearraysetrecordinfo, oleauto/SafeArraySetRecordInfo
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
 - SafeArraySetRecordInfo
 - oleauto/SafeArraySetRecordInfo
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
 - SafeArraySetRecordInfo
---

# SafeArraySetRecordInfo function


## -description

Sets the record info in the specified safe array.

## -parameters

### -param psa [in]

The array descriptor.

### -param prinfo [in]

The record info.

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
The argument <i>psa</i> is null or the array descriptor does not have the FADF_RECORD flag set.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>