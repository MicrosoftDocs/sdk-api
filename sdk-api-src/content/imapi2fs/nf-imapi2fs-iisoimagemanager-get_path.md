---
UID: NF:imapi2fs.IIsoImageManager.get_Path
title: IIsoImageManager::get_Path (imapi2fs.h)
description: Retrieves the logical path to an .iso image.
helpviewer_keywords: ["IIsoImageManager interface [IMAPI]","get_Path method","IIsoImageManager.get_Path","IIsoImageManager::get_Path","get_Path","get_Path method [IMAPI]","get_Path method [IMAPI]","IIsoImageManager interface","imapi.iisoimagemanager_get_path","imapi2fs/IIsoImageManager::get_Path"]
old-location: imapi\iisoimagemanager_get_path.htm
tech.root: imapi
ms.assetid: 56166789-8eeb-4468-a85e-b35e665170d6
ms.date: 12/05/2018
ms.keywords: IIsoImageManager interface [IMAPI],get_Path method, IIsoImageManager.get_Path, IIsoImageManager::get_Path, get_Path, get_Path method [IMAPI], get_Path method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_get_path, imapi2fs/IIsoImageManager::get_Path
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
 - IIsoImageManager::get_Path
 - imapi2fs/IIsoImageManager::get_Path
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
 - IIsoImageManager.get_Path
---

# IIsoImageManager::get_Path


## -description

Retrieves the logical path to an .iso image.

## -parameters

### -param pVal [out]

Pointer to the logical path to an .iso image. For example, "c:\\path\\file.iso".

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager">IIsoImageManager</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath">IIsoImageManager::SetPath</a>