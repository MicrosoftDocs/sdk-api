---
UID: NF:imapi2fs.IFsiNamedStreams.get_Item
title: IFsiNamedStreams::get_Item (imapi2fs.h)
description: Retrieves a single named stream associated with a file in the file system image.
helpviewer_keywords: ["IFsiNamedStreams interface [IMAPI]","get_Item method","IFsiNamedStreams.get_Item","IFsiNamedStreams::get_Item","get_Item","get_Item method [IMAPI]","get_Item method [IMAPI]","IFsiNamedStreams interface","imapi.ifsinamedstreams_get_item","imapi2fs/IFsiNamedStreams::get_Item"]
old-location: imapi\ifsinamedstreams_get_item.htm
tech.root: imapi
ms.assetid: e5ab97cc-cc5a-4fc5-b79a-f1e0a8647c77
ms.date: 12/05/2018
ms.keywords: IFsiNamedStreams interface [IMAPI],get_Item method, IFsiNamedStreams.get_Item, IFsiNamedStreams::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IFsiNamedStreams interface, imapi.ifsinamedstreams_get_item, imapi2fs/IFsiNamedStreams::get_Item
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
 - IFsiNamedStreams::get_Item
 - imapi2fs/IFsiNamedStreams::get_Item
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
 - IFsiNamedStreams.get_Item
---

# IFsiNamedStreams::get_Item


## -description

Retrieves a  single named stream associated with a file in the file system image.

## -parameters

### -param index [in]

This value indicates the position of the named stream within the  collection.
	The index number is zero-based, i.e. the first item is at location 0 of the collection.

### -param item [out, optional]

Pointer to a pointer to an <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2">IFsiFileItem2</a> object representing the named stream at the  position specified by <i>index</i>. This parameter is set to <b>NULL</b> if the specified index is not within the collection boundary.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
<dt>Value: 0xC0AAB101</dt>
</dl>
</td>
<td width="60%">
The value specified for parameter '<i>%1!ls!</i>' is invalid.

</td>
</tr>
</table>

## -remarks

If the index number is negative or out of range, this method returns the <b>IMAPI_E_INVALID_PARAM</b>.

To fetch an <b>IEnumVARIANT</b> enumerator for all named streams associated with a file, use the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsinamedstreams-get__newenum">IFsiNamedStreams::get__NewEnum</a> method.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams">IFsiNamedStreams</a>