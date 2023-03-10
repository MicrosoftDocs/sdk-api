---
UID: NE:imapi2fs.FsiItemType
title: FsiItemType (imapi2fs.h)
description: Defines values for the file system item that was found using the IFileSystemImage::Exists method.
helpviewer_keywords: ["FsiItemDirectory","FsiItemFile","FsiItemNotFound","FsiItemType","FsiItemType enumeration [IMAPI]","imapi.fsiitemtype","imapi2fs/FsiItemDirectory","imapi2fs/FsiItemFile","imapi2fs/FsiItemNotFound","imapi2fs/FsiItemType"]
old-location: imapi\fsiitemtype.htm
tech.root: imapi
ms.assetid: b0ddf0fc-30db-464d-8761-da400386a609
ms.date: 12/05/2018
ms.keywords: FsiItemDirectory, FsiItemFile, FsiItemNotFound, FsiItemType, FsiItemType enumeration [IMAPI], imapi.fsiitemtype, imapi2fs/FsiItemDirectory, imapi2fs/FsiItemFile, imapi2fs/FsiItemNotFound, imapi2fs/FsiItemType
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
req.typenames: FsiItemType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FsiItemType
 - imapi2fs/FsiItemType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2fs.h
api_name:
 - FsiItemType
---

# FsiItemType enumeration


## -description

Defines values for the file system item that was found using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-exists">IFileSystemImage::Exists</a> method.

## -enum-fields

### -field FsiItemNotFound:0

The specified item was not found.

### -field FsiItemDirectory:1

The specified item is a directory.

### -field FsiItemFile:2

The specified item is a file.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-exists">IFileSystemImage::Exists</a>
