---
UID: NF:oaidl.IRecordInfo.GetSize
title: IRecordInfo::GetSize (oaidl.h)
description: Gets the number of bytes of memory necessary to hold the record instance.
helpviewer_keywords: ["GetSize","GetSize method [Automation]","GetSize method [Automation]","IRecordInfo interface","IRecordInfo interface [Automation]","GetSize method","IRecordInfo.GetSize","IRecordInfo::GetSize","_oa96_IRecordInfo_GetSize","automat.irecordinfo_getsize","oaidl/IRecordInfo::GetSize"]
old-location: automat\irecordinfo_getsize.htm
tech.root: automat
ms.assetid: ca0f43b2-2b8f-4b22-8674-8223f0c607ab
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Automation], GetSize method [Automation],IRecordInfo interface, IRecordInfo interface [Automation],GetSize method, IRecordInfo.GetSize, IRecordInfo::GetSize, _oa96_IRecordInfo_GetSize, automat.irecordinfo_getsize, oaidl/IRecordInfo::GetSize
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
 - IRecordInfo::GetSize
 - oaidl/IRecordInfo::GetSize
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
 - IRecordInfo.GetSize
---

# IRecordInfo::GetSize


## -description

Gets the number of bytes of memory necessary to hold the record instance. This allows you to allocate memory for a record instance rather than calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-irecordinfo-recordcreate">RecordCreate</a>.

## -parameters

### -param pcbSize [out]

The size of a record instance, in bytes.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a>