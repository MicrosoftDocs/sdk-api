---
UID: NF:imapi2fs.IFsiNamedStreams.get__NewEnum
title: IFsiNamedStreams::get__NewEnum (imapi2fs.h)
description: Retrieves an IEnumVARIANT list of the named streams associated with a file in the file system image.
helpviewer_keywords: ["IFsiNamedStreams interface [IMAPI]","get__NewEnum method","IFsiNamedStreams.get__NewEnum","IFsiNamedStreams::get__NewEnum","get__NewEnum","get__NewEnum method [IMAPI]","get__NewEnum method [IMAPI]","IFsiNamedStreams interface","imapi.ifsinamedstreams_get_newenum","imapi2fs/IFsiNamedStreams::get__NewEnum"]
old-location: imapi\ifsinamedstreams_get_newenum.htm
tech.root: imapi
ms.assetid: ea1a14fe-91f0-4710-9d15-66a4c415f541
ms.date: 12/05/2018
ms.keywords: IFsiNamedStreams interface [IMAPI],get__NewEnum method, IFsiNamedStreams.get__NewEnum, IFsiNamedStreams::get__NewEnum, get__NewEnum, get__NewEnum method [IMAPI], get__NewEnum method [IMAPI],IFsiNamedStreams interface, imapi.ifsinamedstreams_get_newenum, imapi2fs/IFsiNamedStreams::get__NewEnum
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IFsiNamedStreams::get__NewEnum
 - imapi2fs/IFsiNamedStreams::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiNamedStreams.get__NewEnum
---

# IFsiNamedStreams::get__NewEnum


## -description

Retrieves an <b>IEnumVARIANT</b> list of the named streams associated with a file in the file system image.

## -parameters

### -param NewEnum [out, optional]

Pointer to a pointer to an <b>IEnumVariant</b> interface that is used to enumerate the named streams associated with a file. The items of the enumeration are variants whose type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to retrieve the path to the named stream.

## -returns

S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements. The <i>celt</i> and <i>pceltFetched</i> parameters are defined by <b>IEnumVariant</b>.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>Value: 0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Failed to allocate required memory.

</td>
</tr>
</table>

## -remarks

The enumeration is a snapshot of the named streams associated with the file at the time of the call and will not reflect named streams that are added or removed later on.

To retrieve a single named stream, use the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsinamedstreams-get_item">IFsiNamedStreams::get_Item</a> method.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams">IFsiNamedStreams</a>