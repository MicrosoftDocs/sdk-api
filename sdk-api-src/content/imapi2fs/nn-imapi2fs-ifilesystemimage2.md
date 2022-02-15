---
UID: NN:imapi2fs.IFileSystemImage2
title: IFileSystemImage2 (imapi2fs.h)
description: Use this interface to write multiple boot entries or boot images required for the EFI/UEFI support. For example, boot media with boot straps for both Windows XP and Windows Vista.
helpviewer_keywords: ["IFileSystemImage2","IFileSystemImage2 interface [IMAPI]","IFileSystemImage2 interface [IMAPI]","described","imapi.ifilesystemimage2","imapi2fs/IFileSystemImage2"]
old-location: imapi\ifilesystemimage2.htm
tech.root: imapi
ms.assetid: c38995b7-6f32-4489-bb6c-0e3561b11f81
ms.date: 12/05/2018
ms.keywords: IFileSystemImage2, IFileSystemImage2 interface [IMAPI], IFileSystemImage2 interface [IMAPI],described, imapi.ifilesystemimage2, imapi2fs/IFileSystemImage2
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFileSystemImage2
 - imapi2fs/IFileSystemImage2
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
 - IFileSystemImage2
---

# IFileSystemImage2 interface


## -description

 Use this interface to write multiple boot entries or boot images  required for the EFI/UEFI support. For example, boot media with boot straps for both Windows XP and Windows Vista.<div class="alert"><b>Note</b>  The <b>IFileSystemImage2</b> interface is currently only available with  Windows Vista with Service Pack 1 (SP1) and  Windows Server 2008.</div>
<div> </div>

## -inheritance

The <b>IFileSystemImage2</b> interface inherits from <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>. <b>IFileSystemImage2</b> also has these types of members:

## -remarks

 Boot entries are limited by the interface to 32 per disc.	The boot image must be supplied to IMAPIv2FS by outside applications who invoke IMAPIv2FS to build the bootable disc.

Section Entry Extension is not supported by IMAPIv2FS at this time.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>
