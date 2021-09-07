---
UID: NN:imapi2fs.IFileSystemImageResult
title: IFileSystemImageResult (imapi2fs.h)
description: Use this interface to get information about the burn image, the image data stream, and progress information.
helpviewer_keywords: ["IFileSystemImageResult","IFileSystemImageResult interface [IMAPI]","IFileSystemImageResult interface [IMAPI]","described","imapi.ifilesystemimageresult","imapi2fs/IFileSystemImageResult"]
old-location: imapi\ifilesystemimageresult.htm
tech.root: imapi
ms.assetid: 30ec514c-97b8-41fc-b814-11f50cacaa25
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult, IFileSystemImageResult interface [IMAPI], IFileSystemImageResult interface [IMAPI],described, imapi.ifilesystemimageresult, imapi2fs/IFileSystemImageResult
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
 - IFileSystemImageResult
 - imapi2fs/IFileSystemImageResult
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
 - IFileSystemImageResult
---

# IFileSystemImageResult interface


## -description

Use this interface to get information about the burn image, the image data stream, and progress information.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">IFileSystemImage::CreateResultImage</a> method.

## -inheritance

The <b>IFileSystemImageResult</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFileSystemImageResult</b> also has these types of members:

## -remarks

This is an <b>FileSystemImageResult</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">IFileSystemImage::CreateResultImage</a>
