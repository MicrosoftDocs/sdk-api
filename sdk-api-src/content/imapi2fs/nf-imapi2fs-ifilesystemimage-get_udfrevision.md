---
UID: NF:imapi2fs.IFileSystemImage.get_UDFRevision
title: IFileSystemImage::get_UDFRevision (imapi2fs.h)
description: Retrieves the UDF revision level of the imported file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_UDFRevision method","IFileSystemImage.get_UDFRevision","IFileSystemImage::get_UDFRevision","get_UDFRevision","get_UDFRevision method [IMAPI]","get_UDFRevision method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_udfrevision","imapi2fs/IFileSystemImage::get_UDFRevision"]
old-location: imapi\ifilesystemimage_get_udfrevision.htm
tech.root: imapi
ms.assetid: c854a8db-730a-42a3-b50c-fb8fec271b57
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UDFRevision method, IFileSystemImage.get_UDFRevision, IFileSystemImage::get_UDFRevision, get_UDFRevision, get_UDFRevision method [IMAPI], get_UDFRevision method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_udfrevision, imapi2fs/IFileSystemImage::get_UDFRevision
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
 - IFileSystemImage::get_UDFRevision
 - imapi2fs/IFileSystemImage::get_UDFRevision
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
 - IFileSystemImage.get_UDFRevision
---

# IFileSystemImage::get_UDFRevision


## -description

Retrieves the UDF revision level of the imported file system image.

## -parameters

### -param pVal [out]

UDF revision level of the imported file system image.

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



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_udfrevision">IFileSystemImage::put_UDFRevision</a>