---
UID: NF:imapi2fs.IIsoImageManager.Validate
title: IIsoImageManager::Validate (imapi2fs.h)
description: Determines if the provided .iso image is valid.
helpviewer_keywords: ["IIsoImageManager interface [IMAPI]","Validate method","IIsoImageManager.Validate","IIsoImageManager::Validate","Validate","Validate method [IMAPI]","Validate method [IMAPI]","IIsoImageManager interface","imapi.iisoimagemanager_validate","imapi2fs/IIsoImageManager::Validate"]
old-location: imapi\iisoimagemanager_validate.htm
tech.root: imapi
ms.assetid: 0fd9f0fc-8a77-4b94-9111-c8ce223329b6
ms.date: 12/05/2018
ms.keywords: IIsoImageManager interface [IMAPI],Validate method, IIsoImageManager.Validate, IIsoImageManager::Validate, Validate, Validate method [IMAPI], Validate method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_validate, imapi2fs/IIsoImageManager::Validate
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IIsoImageManager::Validate
 - imapi2fs/IIsoImageManager::Validate
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
 - IIsoImageManager.Validate
---

# IIsoImageManager::Validate


## -description

Determines if the provided .iso image is valid.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</b></dt>
</dl>
</td>
<td width="60%">
The image is not aligned on a 2kb sector boundary.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The image does not contain a valid volume descriptor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_NO_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath">SetPath</a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream">SetStream</a> method prior to calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
The provided image is too large to be validated as the size exceeds MAXLONG.

</td>
</tr>
</table>

## -remarks

For this method to succeed, the disc image, which may be a file or a stream, must meet the following criteria:<ul>
<li>The disc image size must be a multiple of the sector user data size, 2048 bytes.</li>
<li>The disc image must contain user data only and no sector header or file header.</li>
<li>The disc image must contain a valid Volume Recognition Sequence with at least one Volume Descriptor such as described in ECMA <a href="https://www.ecma-international.org/publications/standards/Ecma-119.htm">119</a>, <a href="https://www.ecma-international.org/publications/standards/Ecma-167.htm">167</a>, <a href="https://www.ecma-international.org/publications/standards/Ecma-168.htm">168</a> standards.</li>
</ul> 
 
If the disc image does not fit these criteria, this method will return the relevant failure code. More importantly, a failure to validate will affect the probability of operation success when the image is mounted by Windows after recording.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager">IIsoImageManager</a>
