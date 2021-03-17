---
UID: NF:imapi2fs.IFileSystemImage.get_UDFRevisionsSupported
title: IFileSystemImage::get_UDFRevisionsSupported (imapi2fs.h)
description: Retrieves a list of supported UDF revision levels.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_UDFRevisionsSupported method","IFileSystemImage.get_UDFRevisionsSupported","IFileSystemImage::get_UDFRevisionsSupported","get_UDFRevisionsSupported","get_UDFRevisionsSupported method [IMAPI]","get_UDFRevisionsSupported method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_udfrevisionssupported","imapi2fs/IFileSystemImage::get_UDFRevisionsSupported"]
old-location: imapi\ifilesystemimage_get_udfrevisionssupported.htm
tech.root: imapi
ms.assetid: ad9b4a68-5fef-4092-9cef-4b5ebd9c5093
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UDFRevisionsSupported method, IFileSystemImage.get_UDFRevisionsSupported, IFileSystemImage::get_UDFRevisionsSupported, get_UDFRevisionsSupported, get_UDFRevisionsSupported method [IMAPI], get_UDFRevisionsSupported method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_udfrevisionssupported, imapi2fs/IFileSystemImage::get_UDFRevisionsSupported
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
 - IFileSystemImage::get_UDFRevisionsSupported
 - imapi2fs/IFileSystemImage::get_UDFRevisionsSupported
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
 - IFileSystemImage.get_UDFRevisionsSupported
---

# IFileSystemImage::get_UDFRevisionsSupported


## -description

Retrieves a list of supported UDF revision levels.

## -parameters

### -param pVal [out]

List of supported UDF revision levels. Each element of the list is VARIANT. The variant type is <b>VT_I4</b>. The <b>lVal</b> member of the variant contains the revision level.

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
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -remarks

The value is encoded according to the UDF specification, except the variable size is LONG. For example, revision level 1.02 is represented as 0x102.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_udfrevision">IFileSystemImage::get_UDFRevision</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_udfrevision">IFileSystemImage::put_UDFRevision</a>