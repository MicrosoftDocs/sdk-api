---
UID: NF:imapi2fs.IFileSystemImage.get_ISO9660InterchangeLevelsSupported
title: IFileSystemImage::get_ISO9660InterchangeLevelsSupported (imapi2fs.h)
description: Retrieves the supported ISO9660 compatibility levels.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_ISO9660InterchangeLevelsSupported method","IFileSystemImage.get_ISO9660InterchangeLevelsSupported","IFileSystemImage::get_ISO9660InterchangeLevelsSupported","get_ISO9660InterchangeLevelsSupported","get_ISO9660InterchangeLevelsSupported method [IMAPI]","get_ISO9660InterchangeLevelsSupported method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_iso9660interchangelevelssupported","imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevelsSupported"]
old-location: imapi\ifilesystemimage_get_iso9660interchangelevelssupported.htm
tech.root: imapi
ms.assetid: fd19c3ce-ef84-4f15-9032-679115b8b21f
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_ISO9660InterchangeLevelsSupported method, IFileSystemImage.get_ISO9660InterchangeLevelsSupported, IFileSystemImage::get_ISO9660InterchangeLevelsSupported, get_ISO9660InterchangeLevelsSupported, get_ISO9660InterchangeLevelsSupported method [IMAPI], get_ISO9660InterchangeLevelsSupported method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_iso9660interchangelevelssupported, imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevelsSupported
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
 - IFileSystemImage::get_ISO9660InterchangeLevelsSupported
 - imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevelsSupported
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
 - IFileSystemImage.get_ISO9660InterchangeLevelsSupported
---

# IFileSystemImage::get_ISO9660InterchangeLevelsSupported


## -description

Retrieves the supported ISO9660 compatibility levels.

## -parameters

### -param pVal [out]

List of supported ISO9660 compatibility levels. Each item in the list is a VARIANT that identifies one supported interchange level. The variant type is <b>VT_UI4</b>. The <b>ulVal</b> member of the variant contains the compatibility level.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevel">IFileSystemImage::get_ISO9660InterchangeLevel</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_iso9660interchangelevel">IFileSystemImage::put_ISO9660InterchangeLevel</a>