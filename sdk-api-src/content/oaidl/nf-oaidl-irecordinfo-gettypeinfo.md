---
UID: NF:oaidl.IRecordInfo.GetTypeInfo
title: IRecordInfo::GetTypeInfo (oaidl.h)
description: Retrieves the type information that describes a UDT or safearray of UDTs.
helpviewer_keywords: ["GetTypeInfo","GetTypeInfo method [Automation]","GetTypeInfo method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetTypeInfo method","IRecordInfo.GetTypeInfo","IRecordInfo::GetTypeInfo","_oa96_IRecordInfo_GetTypeInfo","automat.irecordinfo_gettypeinfo","oaidl/IRecordInfo::GetTypeInfo"]
old-location: automat\irecordinfo_gettypeinfo.htm
tech.root: automat
ms.assetid: c8c05c4a-000a-4e48-aace-ff9f9292e3ea
ms.date: 12/05/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Automation], GetTypeInfo method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetTypeInfo method, IRecordInfo.GetTypeInfo, IRecordInfo::GetTypeInfo, _oa96_IRecordInfo_GetTypeInfo, automat.irecordinfo_gettypeinfo, oaidl/IRecordInfo::GetTypeInfo
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - IRecordInfo::GetTypeInfo
 - oaidl/IRecordInfo::GetTypeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IRecordInfo.GetTypeInfo
---

# IRecordInfo::GetTypeInfo


## -description

Retrieves the type information that describes a UDT or safearray of UDTs.

## -parameters

### -param ppTypeInfo [out]

The information type of the record.

## -returns

This method can return one of these values.

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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.


</td>
</tr>
</table>

## -remarks

<b>AddRef</b> is called on the pointer <i>ppTypeInfo</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>