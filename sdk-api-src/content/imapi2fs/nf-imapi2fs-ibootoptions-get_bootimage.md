---
UID: NF:imapi2fs.IBootOptions.get_BootImage
title: IBootOptions::get_BootImage (imapi2fs.h)
description: Retrieves a pointer to the boot image data stream.
helpviewer_keywords: ["IBootOptions interface [IMAPI]","get_BootImage method","IBootOptions.get_BootImage","IBootOptions::get_BootImage","get_BootImage","get_BootImage method [IMAPI]","get_BootImage method [IMAPI]","IBootOptions interface","imapi.ibootoptions_get_bootimage","imapi2fs/IBootOptions::get_BootImage"]
old-location: imapi\ibootoptions_get_bootimage.htm
tech.root: imapi
ms.assetid: 161e0cea-63dd-4806-a246-4b36249b2cc7
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],get_BootImage method, IBootOptions.get_BootImage, IBootOptions::get_BootImage, get_BootImage, get_BootImage method [IMAPI], get_BootImage method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_bootimage, imapi2fs/IBootOptions::get_BootImage
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
 - IBootOptions::get_BootImage
 - imapi2fs/IBootOptions::get_BootImage
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
 - IBootOptions.get_BootImage
---

# IBootOptions::get_BootImage


## -description

Retrieves a pointer to the boot image data stream.

## -parameters

### -param pVal [out]

Pointer to the <b>IStream</b> interface associated with the boot image data stream.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-assignbootimage">IBootOptions::AssignBootImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_bootimageoptions">IFileSystemImage::get_BootImageOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">IFileSystemImage::put_BootImageOptions</a>