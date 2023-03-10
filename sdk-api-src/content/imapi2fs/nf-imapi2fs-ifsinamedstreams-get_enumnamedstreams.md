---
UID: NF:imapi2fs.IFsiNamedStreams.get_EnumNamedStreams
title: IFsiNamedStreams::get_EnumNamedStreams (imapi2fs.h)
description: Creates a non-variant enumerator for the collection of the named streams associated with a file in the file system image.
helpviewer_keywords: ["IFsiNamedStreams interface [IMAPI]","get_EnumNamedStreams method","IFsiNamedStreams.get_EnumNamedStreams","IFsiNamedStreams::get_EnumNamedStreams","get_EnumNamedStreams","get_EnumNamedStreams method [IMAPI]","get_EnumNamedStreams method [IMAPI]","IFsiNamedStreams interface","imapi.ifsinamedstreams_get_enumnamedstreams","imapi2fs/IFsiNamedStreams::get_EnumNamedStreams"]
old-location: imapi\ifsinamedstreams_get_enumnamedstreams.htm
tech.root: imapi
ms.assetid: 99691d12-bff6-4d75-b9ef-bd92f8198ae2
ms.date: 12/05/2018
ms.keywords: IFsiNamedStreams interface [IMAPI],get_EnumNamedStreams method, IFsiNamedStreams.get_EnumNamedStreams, IFsiNamedStreams::get_EnumNamedStreams, get_EnumNamedStreams, get_EnumNamedStreams method [IMAPI], get_EnumNamedStreams method [IMAPI],IFsiNamedStreams interface, imapi.ifsinamedstreams_get_enumnamedstreams, imapi2fs/IFsiNamedStreams::get_EnumNamedStreams
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
 - IFsiNamedStreams::get_EnumNamedStreams
 - imapi2fs/IFsiNamedStreams::get_EnumNamedStreams
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
 - IFsiNamedStreams.get_EnumNamedStreams
---

# IFsiNamedStreams::get_EnumNamedStreams


## -description

Creates a non-variant enumerator for the collection of the named streams associated with a file in the file system image.

## -parameters

### -param NewEnum [out, optional]

Pointer to a pointer to an <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems">IEnumFsiItems</a> object representing a collection of named streams associated with a file.

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

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams">IFsiNamedStreams</a>