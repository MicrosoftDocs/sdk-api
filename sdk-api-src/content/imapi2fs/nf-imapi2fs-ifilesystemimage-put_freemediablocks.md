---
UID: NF:imapi2fs.IFileSystemImage.put_FreeMediaBlocks
title: IFileSystemImage::put_FreeMediaBlocks (imapi2fs.h)
description: Sets the maximum number of blocks available for the image.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_FreeMediaBlocks method","IFileSystemImage.put_FreeMediaBlocks","IFileSystemImage::put_FreeMediaBlocks","imapi.ifilesystemimage_put_freemediablocks","imapi2fs/IFileSystemImage::put_FreeMediaBlocks","put_FreeMediaBlocks","put_FreeMediaBlocks method [IMAPI]","put_FreeMediaBlocks method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_freemediablocks.htm
tech.root: imapi
ms.assetid: 7ffa2736-6480-4bda-8144-b949bf43e580
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_FreeMediaBlocks method, IFileSystemImage.put_FreeMediaBlocks, IFileSystemImage::put_FreeMediaBlocks, imapi.ifilesystemimage_put_freemediablocks, imapi2fs/IFileSystemImage::put_FreeMediaBlocks, put_FreeMediaBlocks, put_FreeMediaBlocks method [IMAPI], put_FreeMediaBlocks method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_FreeMediaBlocks
 - imapi2fs/IFileSystemImage::put_FreeMediaBlocks
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
 - IFileSystemImage.put_FreeMediaBlocks
---

# IFileSystemImage::put_FreeMediaBlocks


## -description

Sets the maximum number of blocks available for the image.

## -parameters

### -param newVal [in]

Number of blocks to use in creating the file system image. 

By default, 332,800 blocks are used to create the file system image. This value assumes a capacity of 74 minutes of audio per 650MB disc.

To specify an infinite number of block, set <i>newVal</i> to zero.

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
<dt><b>IMAPI_E_IMAGE_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
Value specified for FreeMediaBlocks property is too small for estimated image size based on current data. 

Value: 0xC0AAB121

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_freemediablocks">IFileSystemImage::get_FreeMediaBlocks</a>