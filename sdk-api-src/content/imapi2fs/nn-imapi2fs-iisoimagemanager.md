---
UID: NN:imapi2fs.IIsoImageManager
title: IIsoImageManager (imapi2fs.h)
description: Use this interface to verify if an existing .iso file contains a valid file system for burning.
helpviewer_keywords: ["IIsoImageManager","IIsoImageManager interface [IMAPI]","IIsoImageManager interface [IMAPI]","described","imapi.iisoimagemanager","imapi2fs/IIsoImageManager"]
old-location: imapi\iisoimagemanager.htm
tech.root: imapi
ms.assetid: 47b059a9-a18a-4f32-9a02-6566175ca86b
ms.date: 12/05/2018
ms.keywords: IIsoImageManager, IIsoImageManager interface [IMAPI], IIsoImageManager interface [IMAPI],described, imapi.iisoimagemanager, imapi2fs/IIsoImageManager
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
 - IIsoImageManager
 - imapi2fs/IIsoImageManager
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
 - IIsoImageManager
---

# IIsoImageManager interface


## -description

Use this interface to verify if an existing .iso file contains a valid file system for burning.

## -inheritance

The <b>IIsoImageManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IIsoImageManager</b> also has these types of members:

## -remarks

If a valid path is provided via <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath">SetPath</a>, an <b>IStream</b> object will be created from the supplied image file and the <b>Stream</b> property will be populated.
If a valid <b>IStream</b> is provided via <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream">SetStream</a>, it will be used directly for image validation and the <b>Path</b> property will not be populated.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.
