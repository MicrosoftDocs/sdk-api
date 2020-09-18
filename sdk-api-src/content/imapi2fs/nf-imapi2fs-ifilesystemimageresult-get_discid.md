---
UID: NF:imapi2fs.IFileSystemImageResult.get_DiscId
title: IFileSystemImageResult::get_DiscId (imapi2fs.h)
description: Retrieves the disc volume name for this file system image.
helpviewer_keywords: ["IFileSystemImageResult interface [IMAPI]","get_DiscId method","IFileSystemImageResult.get_DiscId","IFileSystemImageResult::get_DiscId","get_DiscId","get_DiscId method [IMAPI]","get_DiscId method [IMAPI]","IFileSystemImageResult interface","imapi.ifilesystemimageresult_get_discid","imapi2fs/IFileSystemImageResult::get_DiscId"]
old-location: imapi\ifilesystemimageresult_get_discid.htm
tech.root: imapi
ms.assetid: 2288b4e4-6f36-4830-a077-dcf710741911
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_DiscId method, IFileSystemImageResult.get_DiscId, IFileSystemImageResult::get_DiscId, get_DiscId, get_DiscId method [IMAPI], get_DiscId method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_discid, imapi2fs/IFileSystemImageResult::get_DiscId
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
 - IFileSystemImageResult::get_DiscId
 - imapi2fs/IFileSystemImageResult::get_DiscId
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
 - IFileSystemImageResult.get_DiscId
---

# IFileSystemImageResult::get_DiscId


## -description

Retrieves the disc volume name for this file system image.

## -parameters

### -param pVal [out]

String that contains the volume name for this file system image.

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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">IFileSystemImage::get_VolumeName</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>