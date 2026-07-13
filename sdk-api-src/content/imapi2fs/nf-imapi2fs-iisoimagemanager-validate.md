---
UID: NF:imapi2fs.IIsoImageManager.Validate
title: IIsoImageManager::Validate (imapi2fs.h)
description: Determines if the provided .iso image is valid.
helpviewer_keywords: ["IIsoImageManager interface [IMAPI]","Validate method","IIsoImageManager.Validate","IIsoImageManager::Validate","Validate","Validate method [IMAPI]","Validate method [IMAPI]","IIsoImageManager interface","imapi.iisoimagemanager_validate","imapi2fs/IIsoImageManager::Validate"]
old-location: imapi\iisoimagemanager_validate.htm
tech.root: imapi
ms.assetid: 0fd9f0fc-8a77-4b94-9111-c8ce223329b6
ms.date: 10/03/2024
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

| Return code | Description |
|-------------|-------------|
| **IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED** | The image is not aligned on a 2kb sector boundary. |
| **IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND** | The image does not contain a valid volume descriptor. |
| **IMAPI_E_IMAGEMANAGER_NO_IMAGE** | The image has not been set using the [SetPath](/windows/win32/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath) or [SetStream](/windows/win32/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream) method prior to calling this method. |
| **IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG** | The provided image is too large to be validated as the size exceeds MAXLONG. |

## -remarks

For this method to succeed, the disc image, which may be a file or a stream, must meet the following criteria:

- The disc image size must be a multiple of the sector user data size, 2048 bytes.
- The disc image must contain user data only and no sector header or file header.
- The disc image must contain a valid Volume Recognition Sequence with at least one Volume Descriptor such as described in ECMA [119](https://www.ecma-international.org/wp-content/uploads/ECMA-119_2nd_edition_december_1987.pdf), [167](https://www.ecma-international.org/publications-and-standards/standards/ecma-167/), [168](https://www.ecma-international.org/publications-and-standards/standards/ecma-168/) standards.

If the disc image does not fit these criteria, this method will return the relevant failure code. More importantly, a failure to validate will affect the probability of operation success when the image is mounted by Windows after recording.

## -see-also

- [IIsoImageManager](/windows/win32/api/imapi2fs/nn-imapi2fs-iisoimagemanager)
- [SetPath](/windows/win32/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath)
- [SetStream](/windows/win32/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream)
