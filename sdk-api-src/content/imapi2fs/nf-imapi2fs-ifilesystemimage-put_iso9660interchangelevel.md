---
UID: NF:imapi2fs.IFileSystemImage.put_ISO9660InterchangeLevel
title: IFileSystemImage::put_ISO9660InterchangeLevel (imapi2fs.h)
description: Sets the ISO9660 compatibility level of the file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_ISO9660InterchangeLevel method","IFileSystemImage.put_ISO9660InterchangeLevel","IFileSystemImage::put_ISO9660InterchangeLevel","imapi.ifilesystemimage_put_iso9660interchangelevel","imapi2fs/IFileSystemImage::put_ISO9660InterchangeLevel","put_ISO9660InterchangeLevel","put_ISO9660InterchangeLevel method [IMAPI]","put_ISO9660InterchangeLevel method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_iso9660interchangelevel.htm
tech.root: imapi
ms.assetid: 8bfb770a-5a69-4980-94e2-4a3f65caa645
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_ISO9660InterchangeLevel method, IFileSystemImage.put_ISO9660InterchangeLevel, IFileSystemImage::put_ISO9660InterchangeLevel, imapi.ifilesystemimage_put_iso9660interchangelevel, imapi2fs/IFileSystemImage::put_ISO9660InterchangeLevel, put_ISO9660InterchangeLevel, put_ISO9660InterchangeLevel method [IMAPI], put_ISO9660InterchangeLevel method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_ISO9660InterchangeLevel
 - imapi2fs/IFileSystemImage::put_ISO9660InterchangeLevel
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
 - IFileSystemImage.put_ISO9660InterchangeLevel
---

# IFileSystemImage::put_ISO9660InterchangeLevel


## -description

Sets the ISO9660 compatibility level of the file system image.

## -parameters

### -param newVal [in]

ISO9660 compatibility level of the file system image.

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

To determine the supported compatibility levels, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a> method.

This property is meaningful only if you specified FsiFileSystemISO9660 when calling <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">IFileSystemImage::put_FileSystemsToCreate</a>.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevel">IFileSystemImage::get_ISO9660InterchangeLevel</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a>