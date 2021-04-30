---
UID: NF:imapi2fs.IFsiFileItem2.get_FsiNamedStreams
title: IFsiFileItem2::get_FsiNamedStreams (imapi2fs.h)
description: Retrieves a collection of named streams associated with a file in the file system image.
helpviewer_keywords: ["IFsiFileItem2 interface [IMAPI]","get_FsiNamedStreams method","IFsiFileItem2.get_FsiNamedStreams","IFsiFileItem2::get_FsiNamedStreams","get_FsiNamedStreams","get_FsiNamedStreams method [IMAPI]","get_FsiNamedStreams method [IMAPI]","IFsiFileItem2 interface","imapi.ifsifileitem2_get_fsinamedstreams","imapi2fs/IFsiFileItem2::get_FsiNamedStreams"]
old-location: imapi\ifsifileitem2_get_fsinamedstreams.htm
tech.root: imapi
ms.assetid: 011c6241-4989-41ca-9876-d6810797a382
ms.date: 12/05/2018
ms.keywords: IFsiFileItem2 interface [IMAPI],get_FsiNamedStreams method, IFsiFileItem2.get_FsiNamedStreams, IFsiFileItem2::get_FsiNamedStreams, get_FsiNamedStreams, get_FsiNamedStreams method [IMAPI], get_FsiNamedStreams method [IMAPI],IFsiFileItem2 interface, imapi.ifsifileitem2_get_fsinamedstreams, imapi2fs/IFsiFileItem2::get_FsiNamedStreams
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IFsiFileItem2::get_FsiNamedStreams
 - imapi2fs/IFsiFileItem2::get_FsiNamedStreams
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
 - IFsiFileItem2.get_FsiNamedStreams
---

# IFsiFileItem2::get_FsiNamedStreams


## -description

Retrieves a collection of named streams associated with a file in the file system image.

## -parameters

### -param streams [out, optional]

Pointer to an <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams">IFsiNamedStreams</a> object that represents a collection of named streams associated with the file.

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
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b></dt>
<dt>Value: 0xC0AAB160L</dt>
</dl>
</td>
<td width="60%">
Property '<i>%1!ls!</i>' is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>Value: 0x8007000E</dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

</td>
</tr>
</table>

## -remarks

If this method is invoked for a file item which itself represents a named stream, the <b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b> error code is returned, as a named streams cannot contain additional named streams.

The user must enable UDF and set the UDF revision to 2.00 or higher to support named streams.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2">IFsiFileItem2</a>