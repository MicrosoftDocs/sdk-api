---
UID: NF:imapi2fs.IFileSystemImage.put_UDFRevision
title: IFileSystemImage::put_UDFRevision (imapi2fs.h)
description: Sets the UDF revision level of the file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_UDFRevision method","IFileSystemImage.put_UDFRevision","IFileSystemImage::put_UDFRevision","imapi.ifilesystemimage_put_udfrevision","imapi2fs/IFileSystemImage::put_UDFRevision","put_UDFRevision","put_UDFRevision method [IMAPI]","put_UDFRevision method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_udfrevision.htm
tech.root: imapi
ms.assetid: a4b0e73b-6bef-44e1-b0b7-9a4e0fcc1370
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_UDFRevision method, IFileSystemImage.put_UDFRevision, IFileSystemImage::put_UDFRevision, imapi.ifilesystemimage_put_udfrevision, imapi2fs/IFileSystemImage::put_UDFRevision, put_UDFRevision, put_UDFRevision method [IMAPI], put_UDFRevision method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_UDFRevision
 - imapi2fs/IFileSystemImage::put_UDFRevision
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
 - IFileSystemImage.put_UDFRevision
---

# IFileSystemImage::put_UDFRevision


## -description

Sets the UDF revision level of the file system image.

## -parameters

### -param newVal [in]

A hexadecimal number representing the UDF revision level.

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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>

## -remarks

The value is encoded according to the UDF specification, except the variable size is LONG. For example, revision level 1.02 is represented as 0x102.

This property is used to specify the UDF revision in a new file system image. If the file system is imported, you cannot call this method to change the UDF revision level.

To determine the supported UDF revision levels, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_udfrevisionssupported">IFileSystemImage::get_UDFRevisionsSupported</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_udfrevision">IFileSystemImage::get_UDFRevision</a>