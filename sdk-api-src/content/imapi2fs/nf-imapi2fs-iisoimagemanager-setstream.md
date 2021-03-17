---
UID: NF:imapi2fs.IIsoImageManager.SetStream
title: IIsoImageManager::SetStream (imapi2fs.h)
description: Sets the Stream property with the IStream object associated with the .iso image.
helpviewer_keywords: ["IIsoImageManager interface [IMAPI]","SetStream method","IIsoImageManager.SetStream","IIsoImageManager::SetStream","SetStream","SetStream method [IMAPI]","SetStream method [IMAPI]","IIsoImageManager interface","imapi.iisoimagemanager_setstream","imapi2fs/IIsoImageManager::SetStream"]
old-location: imapi\iisoimagemanager_setstream.htm
tech.root: imapi
ms.assetid: 3ee540aa-8ccc-40cb-afc8-b1790cabee6e
ms.date: 12/05/2018
ms.keywords: IIsoImageManager interface [IMAPI],SetStream method, IIsoImageManager.SetStream, IIsoImageManager::SetStream, SetStream, SetStream method [IMAPI], SetStream method [IMAPI],IIsoImageManager interface, imapi.iisoimagemanager_setstream, imapi2fs/IIsoImageManager::SetStream
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
 - IIsoImageManager::SetStream
 - imapi2fs/IIsoImageManager::SetStream
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
 - IIsoImageManager.SetStream
---

# IIsoImageManager::SetStream


## -description

Sets the <b>Stream</b> property with the <b>IStream</b> object associated with the .iso image.

## -parameters

### -param data [in, optional]

The <b>IStream</b> object associated with the .iso image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager">IIsoImageManager</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-get_stream">IIsoImageManager::get_Stream</a>