---
UID: NF:oleauto.SafeArrayGetRecordInfo
title: SafeArrayGetRecordInfo function (oleauto.h)
description: Retrieves the IRecordInfo interface of the UDT contained in the specified safe array.
helpviewer_keywords: ["SafeArrayGetRecordInfo","SafeArrayGetRecordInfo function [Automation]","_oa96_SafeArrayGetRecordInfo","automat.safearraygetrecordinfo","oleauto/SafeArrayGetRecordInfo"]
old-location: automat\safearraygetrecordinfo.htm
tech.root: automat
ms.assetid: 1584c00e-06a5-44f4-8c4b-a2b23737a652
ms.date: 12/05/2018
ms.keywords: SafeArrayGetRecordInfo, SafeArrayGetRecordInfo function [Automation], _oa96_SafeArrayGetRecordInfo, automat.safearraygetrecordinfo, oleauto/SafeArrayGetRecordInfo
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
 - SafeArrayGetRecordInfo
 - oleauto/SafeArrayGetRecordInfo
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
 - SafeArrayGetRecordInfo
---

# SafeArrayGetRecordInfo function


## -description

Retrieves the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> interface of the UDT contained in the specified safe array.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

### -param prinfo [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> interface.

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