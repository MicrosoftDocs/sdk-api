---
UID: NF:imapi2fs.IBootOptions.AssignBootImage
title: IBootOptions::AssignBootImage (imapi2fs.h)
description: Sets the data stream that contains the boot image.
helpviewer_keywords: ["AssignBootImage","AssignBootImage method [IMAPI]","AssignBootImage method [IMAPI]","IBootOptions interface","IBootOptions interface [IMAPI]","AssignBootImage method","IBootOptions.AssignBootImage","IBootOptions::AssignBootImage","imapi.ibootoptions_assignbootimage","imapi2fs/IBootOptions::AssignBootImage"]
old-location: imapi\ibootoptions_assignbootimage.htm
tech.root: imapi
ms.assetid: 63d598dd-72a8-4544-813d-11f2e7e53ec5
ms.date: 12/05/2018
ms.keywords: AssignBootImage, AssignBootImage method [IMAPI], AssignBootImage method [IMAPI],IBootOptions interface, IBootOptions interface [IMAPI],AssignBootImage method, IBootOptions.AssignBootImage, IBootOptions::AssignBootImage, imapi.ibootoptions_assignbootimage, imapi2fs/IBootOptions::AssignBootImage
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
 - IBootOptions::AssignBootImage
 - imapi2fs/IBootOptions::AssignBootImage
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
 - IBootOptions.AssignBootImage
---

# IBootOptions::AssignBootImage


## -description

Sets the data stream that contains the boot image.

## -parameters

### -param newVal [in]

An <b>IStream</b> interface of the data stream that contains the boot image.

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
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_IMAGE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The boot object could not be added to the image.

Value: 0xC0AAB142

</td>
</tr>
</table>

## -remarks

If the size of the newly assigned boot image is either 1.2, 1.44. or 2.88 MB, this method will automatically adjust the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-emulationtype">EmulationType</a> value to the respective "floppy" type value.   It is, however, possible to  override the default or previously assigned <b>EmulationType</b> value by calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_emulation">IBootOptions::put_Emulation</a> method.

The additional specification of the platform on which to use the boot image requires the call to the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_platformid">IBootOptions::put_PlatformId</a> method.

IMAPI does not include any boot images; developers must provide their own boot images.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_bootimage">IBootOptions::get_BootImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_bootimageoptions">IFileSystemImage::get_BootImageOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">IFileSystemImage::put_BootImageOptions</a>