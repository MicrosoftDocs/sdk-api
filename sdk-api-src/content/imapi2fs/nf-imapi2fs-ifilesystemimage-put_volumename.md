---
UID: NF:imapi2fs.IFileSystemImage.put_VolumeName
title: IFileSystemImage::put_VolumeName (imapi2fs.h)
description: Sets the volume name for this file system image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_VolumeName method","IFileSystemImage.put_VolumeName","IFileSystemImage::put_VolumeName","imapi.ifilesystemimage_put_volumename","imapi2fs/IFileSystemImage::put_VolumeName","put_VolumeName","put_VolumeName method [IMAPI]","put_VolumeName method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_volumename.htm
tech.root: imapi
ms.assetid: afb87eb1-5d14-413a-8830-2612920eac3d
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_VolumeName method, IFileSystemImage.put_VolumeName, IFileSystemImage::put_VolumeName, imapi.ifilesystemimage_put_volumename, imapi2fs/IFileSystemImage::put_VolumeName, put_VolumeName, put_VolumeName method [IMAPI], put_VolumeName method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_VolumeName
 - imapi2fs/IFileSystemImage::put_VolumeName
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
 - IFileSystemImage.put_VolumeName
---

# IFileSystemImage::put_VolumeName


## -description

Sets the volume name for this file system image.

## -parameters

### -param newVal [in]

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
<dt><b>IMAPI_E_INVALID_VOLUME_NAME</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>

## -remarks

The string is limited to 15 characters. For ISO 9660 discs, the volume name can use the following characters:

<ul>
<li>"A" through "Z"</li>
<li>"0" through "9"</li>
<li>"_" (underscore)</li>
</ul>
For Joliet and UDF discs, the volume name can use the following characters:

<ul>
<li>"a" through "z"</li>
<li>"A" through "Z"</li>
<li>"0" through "9"</li>
<li>"." (period)</li>
<li>"_" (underscore)</li>
</ul>
If you do not specify a volume name, a default volume name is generated using the system date and time when the result object is created.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_importedvolumename">IFileSystemImage::get_ImportedVolumeName</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">IFileSystemImage::get_VolumeName</a>