---
UID: NN:imapi2fs.IFileSystemImageResult2
title: IFileSystemImageResult2 (imapi2fs.h)
description: The IFileSystemImageResult2 interface allows the data recorder object to retrieve information about modified blocks in images created for rewritable discs.
helpviewer_keywords: ["IFileSystemImageResult2","IFileSystemImageResult2 interface [IMAPI]","IFileSystemImageResult2 interface [IMAPI]","described","imapi.ifilesystemimageresult2","imapi2fs/IFileSystemImageResult2"]
old-location: imapi\ifilesystemimageresult2.htm
tech.root: imapi
ms.assetid: 83834da1-fa5a-42ef-8e59-7ba133d3e6cb
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult2, IFileSystemImageResult2 interface [IMAPI], IFileSystemImageResult2 interface [IMAPI],described, imapi.ifilesystemimageresult2, imapi2fs/IFileSystemImageResult2
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IFileSystemImageResult2
 - imapi2fs/IFileSystemImageResult2
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
 - IFileSystemImageResult2
---

# IFileSystemImageResult2 interface


## -description

The <b>IFileSystemImageResult2</b> interface allows the data recorder object to retrieve information about modified blocks in images created for rewritable discs. Alternatively, <b>IUnknown::QueryInterface</b> can be called on the object returned by <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_imagestream">IFileSystemImageResult::get_ImageStream</a> to get the <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a> interface providing this information.

## -inheritance

The <b>IFileSystemImageResult2</b> interface inherits from <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>. <b>IFileSystemImageResult2</b> also has these types of members:

## -remarks

When the file system image object is used to append data to a rewritable disc, the result image contains both the previous logical session and the new additions. The result image represents the binary data that must be recorded to disc starting from sector 0 to get a disc containing both old and new files. However, the previous logical session remains mostly intact during addition of new files, so the burn time can be substantially optimized by recording only the sectors that are new or have been modified.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>
