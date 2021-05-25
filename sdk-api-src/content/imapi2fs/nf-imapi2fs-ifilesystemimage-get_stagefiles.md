---
UID: NF:imapi2fs.IFileSystemImage.get_StageFiles
title: IFileSystemImage::get_StageFiles (imapi2fs.h)
description: Indicates if the files being added to the file system image should be staged before the burn.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_StageFiles method","IFileSystemImage.get_StageFiles","IFileSystemImage::get_StageFiles","get_StageFiles","get_StageFiles method [IMAPI]","get_StageFiles method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_stagefiles","imapi2fs/IFileSystemImage::get_StageFiles"]
old-location: imapi\ifilesystemimage_get_stagefiles.htm
tech.root: imapi
ms.assetid: 7146ad88-071a-4df9-80f9-46e24b49286b
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_StageFiles method, IFileSystemImage.get_StageFiles, IFileSystemImage::get_StageFiles, get_StageFiles, get_StageFiles method [IMAPI], get_StageFiles method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_stagefiles, imapi2fs/IFileSystemImage::get_StageFiles
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
 - IFileSystemImage::get_StageFiles
 - imapi2fs/IFileSystemImage::get_StageFiles
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
 - IFileSystemImage.get_StageFiles
---

# IFileSystemImage::get_StageFiles


## -description

Indicates if the files being added to the file system image should be staged before the burn.

## -parameters

### -param pVal [out]

<b>VARIANT_TRUE</b> if the files being added to the file system image are required to be staged in one or more stage files before burning. Otherwise, <b>VARIANT_FALSE</b> is returned if IMAPI is permitted to optimize the image creation process by not staging the files being added to the file system image.

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

"Staging" is a process in which an image is created on the hard-drive, containing all files to be burned, prior to the initiation of the  burn operation.

Setting this this property to <b>VARIANT_TRUE</b> via <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_stagefiles">IFileSystemImage::put_StageFiles</a> will only affect files that are added after the property is set: those files will always be staged. Files that were not staged prior  to a specified property value of   <b>VARIANT_TRUE</b>, will not be staged.

By specifying <b>VARIANT_FALSE</b>, the file system image creation process is optimized in two ways:

<ul>
<li>Less time is required for image generation</li>
<li>Less space is consumed on a local disk by IMAPI</li>
</ul>
However, in order to avoid buffer underrun problems during burning, a certain minimum throughput is required for read operations on non-staged files. In the event that file accessibility or throughput may not meet the requirements of the burner, IMAPI enforces file staging regardless of the specified property value. For example, file staging is enforced for source files from removable storage devices, such as USB Flash Disk.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_stagefiles">IFileSystemImage::put_StageFiles</a>