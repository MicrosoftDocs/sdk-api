---
UID: NF:imapi2fs.IFileSystemImage.get_ISO9660InterchangeLevel
title: IFileSystemImage::get_ISO9660InterchangeLevel (imapi2fs.h)
description: Retrieves the ISO9660 compatibility level to use when creating the result image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_ISO9660InterchangeLevel method","IFileSystemImage.get_ISO9660InterchangeLevel","IFileSystemImage::get_ISO9660InterchangeLevel","get_ISO9660InterchangeLevel","get_ISO9660InterchangeLevel method [IMAPI]","get_ISO9660InterchangeLevel method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_iso9660interchangelevel","imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevel"]
old-location: imapi\ifilesystemimage_get_iso9660interchangelevel.htm
tech.root: imapi
ms.assetid: 9536444b-60e4-456f-b6d8-07cf9a6f7848
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_ISO9660InterchangeLevel method, IFileSystemImage.get_ISO9660InterchangeLevel, IFileSystemImage::get_ISO9660InterchangeLevel, get_ISO9660InterchangeLevel, get_ISO9660InterchangeLevel method [IMAPI], get_ISO9660InterchangeLevel method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_iso9660interchangelevel, imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevel
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
 - IFileSystemImage::get_ISO9660InterchangeLevel
 - imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevel
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
 - IFileSystemImage.get_ISO9660InterchangeLevel
---

# IFileSystemImage::get_ISO9660InterchangeLevel


## -description

Retrieves the ISO9660 compatibility level to use when creating the result image.

## -parameters

### -param pVal [out]

Identifies the interchange level of the ISO9660 file system.

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

For a list of supported compatibility levels, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_iso9660interchangelevel">IFileSystemImage::put_ISO9660InterchangeLevel</a>