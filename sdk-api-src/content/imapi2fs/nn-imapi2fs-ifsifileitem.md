---
UID: NN:imapi2fs.IFsiFileItem
title: IFsiFileItem (imapi2fs.h)
description: Use this interface to identify the file size and data stream of the file contents.
helpviewer_keywords: ["IFsiFileItem","IFsiFileItem interface [IMAPI]","IFsiFileItem interface [IMAPI]","described","imapi.ifsifileitem","imapi2fs/IFsiFileItem"]
old-location: imapi\ifsifileitem.htm
tech.root: imapi
ms.assetid: 13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108
ms.date: 12/05/2018
ms.keywords: IFsiFileItem, IFsiFileItem interface [IMAPI], IFsiFileItem interface [IMAPI],described, imapi.ifsifileitem, imapi2fs/IFsiFileItem
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
 - IFsiFileItem
 - imapi2fs/IFsiFileItem
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
 - IFsiFileItem
---

# IFsiFileItem interface


## -description

Use this interface to identify the file size and data stream of the file contents.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem">IFileSystemImage::CreateFileItem</a> method.

## -inheritance

The <b>IFsiFileItem</b> interface inherits from <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>. <b>IFsiFileItem</b> also has these types of members:

## -remarks

Data streams for files contained within the file system image are read-only.  File data can only be replaced by overwriting an existing file item.

This is an <b>FsiFileItem</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>
