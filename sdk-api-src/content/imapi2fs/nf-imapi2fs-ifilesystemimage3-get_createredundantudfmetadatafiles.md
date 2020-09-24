---
UID: NF:imapi2fs.IFileSystemImage3.get_CreateRedundantUdfMetadataFiles
title: IFileSystemImage3::get_CreateRedundantUdfMetadataFiles (imapi2fs.h)
description: Retrieves a property value that specifies if the UDF Metadata will be redundant in the file system image.
helpviewer_keywords: ["IFileSystemImage3 interface [IMAPI]","get_CreateRedundantUdfMetadataFiles method","IFileSystemImage3.get_CreateRedundantUdfMetadataFiles","IFileSystemImage3::get_CreateRedundantUdfMetadataFiles","get_CreateRedundantUdfMetadataFiles","get_CreateRedundantUdfMetadataFiles method [IMAPI]","get_CreateRedundantUdfMetadataFiles method [IMAPI]","IFileSystemImage3 interface","imapi.ifilesystemimage3_get_createredundantudfmetadatafiles","imapi2fs/IFileSystemImage3::get_CreateRedundantUdfMetadataFiles"]
old-location: imapi\ifilesystemimage3_get_createredundantudfmetadatafiles.htm
tech.root: imapi
ms.assetid: d71e997f-e6d6-414b-b89e-73a486f29619
ms.date: 12/05/2018
ms.keywords: IFileSystemImage3 interface [IMAPI],get_CreateRedundantUdfMetadataFiles method, IFileSystemImage3.get_CreateRedundantUdfMetadataFiles, IFileSystemImage3::get_CreateRedundantUdfMetadataFiles, get_CreateRedundantUdfMetadataFiles, get_CreateRedundantUdfMetadataFiles method [IMAPI], get_CreateRedundantUdfMetadataFiles method [IMAPI],IFileSystemImage3 interface, imapi.ifilesystemimage3_get_createredundantudfmetadatafiles, imapi2fs/IFileSystemImage3::get_CreateRedundantUdfMetadataFiles
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
 - IFileSystemImage3::get_CreateRedundantUdfMetadataFiles
 - imapi2fs/IFileSystemImage3::get_CreateRedundantUdfMetadataFiles
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
 - IFileSystemImage3.get_CreateRedundantUdfMetadataFiles
---

# IFileSystemImage3::get_CreateRedundantUdfMetadataFiles


## -description

Retrieves a property value that specifies if the UDF Metadata will be redundant in the file system image.

## -parameters

### -param pVal [out]

Pointer to a value that specifies if the UDF metadata is redundant in the resultant file system image. A value of <b>VARIANT_TRUE</b> indicates that UDF metadata will be redundant; otherwise, <b>VARIANT_FALSE</b>.

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
<dt>(HRESULT) 0x80004003L</dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3">IFileSystemImage3</a>