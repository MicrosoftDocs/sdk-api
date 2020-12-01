---
UID: NF:imapi2fs.IFileSystemImageResult.get_ImageStream
title: IFileSystemImageResult::get_ImageStream (imapi2fs.h)
description: Retrieves the burn image stream.
helpviewer_keywords: ["IFileSystemImageResult interface [IMAPI]","get_ImageStream method","IFileSystemImageResult.get_ImageStream","IFileSystemImageResult::get_ImageStream","get_ImageStream","get_ImageStream method [IMAPI]","get_ImageStream method [IMAPI]","IFileSystemImageResult interface","imapi.ifilesystemimageresult_get_imagestream","imapi2fs/IFileSystemImageResult::get_ImageStream"]
old-location: imapi\ifilesystemimageresult_get_imagestream.htm
tech.root: imapi
ms.assetid: 87e4bde6-c8c3-43b6-b096-514fdef5e262
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_ImageStream method, IFileSystemImageResult.get_ImageStream, IFileSystemImageResult::get_ImageStream, get_ImageStream, get_ImageStream method [IMAPI], get_ImageStream method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_imagestream, imapi2fs/IFileSystemImageResult::get_ImageStream
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
 - IFileSystemImageResult::get_ImageStream
 - imapi2fs/IFileSystemImageResult::get_ImageStream
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
 - IFileSystemImageResult.get_ImageStream
---

# IFileSystemImageResult::get_ImageStream


## -description

Retrieves the burn image stream.

## -parameters

### -param pVal [out]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the burn image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid or the  <i>pstatstgis</i> parameter of the <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> method is <b>NULL</b>.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDFUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>grfStateFlag</i> parameter of the <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> method is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write">IDiscFormat2Data::Write</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>