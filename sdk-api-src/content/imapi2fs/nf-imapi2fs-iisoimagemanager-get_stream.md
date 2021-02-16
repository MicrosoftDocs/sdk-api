---
UID: NF:imapi2fs.IIsoImageManager.get_Stream
title: IIsoImageManager::get_Stream (imapi2fs.h)
description: Retrieves the IStream object associated with the .iso image.
helpviewer_keywords: ["IIsoImageManager interface [IMAPI]","get_Stream method","IIsoImageManager.get_Stream","IIsoImageManager::get_Stream","get_Stream","get_Stream method [IMAPI]","get_Stream method [IMAPI]","IIsoImageManager interface","imapi.iisoimagemanager_get_stream","imapi2fs/IIsoImageManager::get_Stream"]
old-location: imapi\iisoimagemanager_get_stream.htm
tech.root: imapi
ms.assetid: 0655edb2-5dce-4428-b883-984ef53712cd
ms.date: 12/05/2018
ms.keywords: IIsoImageManager interface [IMAPI],get_Stream method, IIsoImageManager.get_Stream, IIsoImageManager::get_Stream, get_Stream, get_Stream method [IMAPI], get_Stream method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_get_stream, imapi2fs/IIsoImageManager::get_Stream
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
 - IIsoImageManager::get_Stream
 - imapi2fs/IIsoImageManager::get_Stream
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
 - IIsoImageManager.get_Stream
---

# IIsoImageManager::get_Stream


## -description

Retrieves the <b>IStream</b> object associated with the .iso image.

## -parameters

### -param data [out]

The <b>IStream</b> object associated with the .iso image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager">IIsoImageManager</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream">IIsoImageManager::SetStream</a>