---
UID: NN:imapi2fs.IBootOptions
title: IBootOptions (imapi2fs.h)
description: Use this interface to specify the boot image to add to the optical disc. A boot image contains one or more sectors of code used to start the computer.helpviewer_keywords: ["IBootOptions","IBootOptions interface [IMAPI]","IBootOptions interface [IMAPI]","described","imapi.ibootoptions","imapi2fs/IBootOptions"]
old-location: imapi\ibootoptions.htm
tech.root: imapi
ms.assetid: 446b535c-d576-4f96-8b74-305e34cb99d4
ms.date: 12/05/2018
ms.keywords: IBootOptions, IBootOptions interface [IMAPI], IBootOptions interface [IMAPI],described, imapi.ibootoptions, imapi2fs/IBootOptions
f1_keywords:
- imapi2fs/IBootOptions
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- imapi2fs.h
api_name:
- IBootOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBootOptions interface


## -description


Use this interface to specify the boot image to add to the optical disc. A boot image contains one or more sectors of code used to start the computer.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(BootOptions) for the class identifier and __uuidof(IBootOptions) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBootOptions</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBootOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBootOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-assignbootimage">AssignBootImage</a>
</td>
<td align="left" width="63%">
Sets the data stream that contains the boot image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_bootimage">get_BootImage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the boot image data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_emulation">get_Emulation</a>
</td>
<td align="left" width="63%">
Retrieves the media type that the boot image is intended to emulate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_imagesize">get_ImageSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the boot image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_manufacturer">get_Manufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the manufacturer of the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_platformid">get_PlatformId</a>
</td>
<td align="left" width="63%">
Retrieves the platform identifier that identifies the operating system architecture that the boot image supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_emulation">put_Emulation</a>
</td>
<td align="left" width="63%">
Sets the media type that the boot image is intended to emulate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_manufacturer">put_Manufacturer</a>
</td>
<td align="left" width="63%">
Sets an identifier that identifies the manufacturer of the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_platformid">put_PlatformId</a>
</td>
<td align="left" width="63%">
Sets the platform identifier that identifies the operating system architecture that the boot image supports.

</td>
</tr>
</table> 


## -remarks



This interface supports the "El Torito" Bootable CD-ROM format specification. 

To add the boot image to a file system image, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">IFileSystemImage::put_BootImageOptions</a> method. 

To get the boot image associated with a file system image, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_bootimageoptions">IFileSystemImage::get_BootImageOptions</a> method.

To create the <b>BootOptions</b> object in a script, use IMAPI2.BootOptions as the program identifier when calling <b>CreateObject</b>.



