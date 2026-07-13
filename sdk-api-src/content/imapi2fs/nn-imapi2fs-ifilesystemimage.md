---
UID: NN:imapi2fs.IFileSystemImage
title: IFileSystemImage (imapi2fs.h)
description: Use this interface to build a file system image, set session parameter, and import or export an image.
helpviewer_keywords: ["IFileSystemImage","IFileSystemImage interface [IMAPI]","IFileSystemImage interface [IMAPI]","described","imapi.ifilesystemimage","imapi2fs/IFileSystemImage"]
old-location: imapi\ifilesystemimage.htm
tech.root: imapi
ms.assetid: 0256f1d2-a3fb-45b2-bd84-e2b71148e4ec
ms.date: 12/05/2018
ms.keywords: IFileSystemImage, IFileSystemImage interface [IMAPI], IFileSystemImage interface [IMAPI],described, imapi.ifilesystemimage, imapi2fs/IFileSystemImage
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
 - IFileSystemImage
 - imapi2fs/IFileSystemImage
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
 - IFileSystemImage
---

# IFileSystemImage interface


## -description

Use this interface to build a file system image, set session parameter, and import or export an image.

The file system directory hierarchy is built by adding directories and files to the root or child directories.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftFileSystemImage) for the class identifier and __uuidof(IFileSystemImage) for the interface identifier.

## -inheritance

The <b>IFileSystemImage</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFileSystemImage</b> also has these types of members:

## -remarks

To create the <b>CFileSystemImage</b> object in a script, use IMAPI2.MsftFileSystemImage as the program identifier when calling <b>CreateObject</b>.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents">DFileSystemImageEvents</a>
