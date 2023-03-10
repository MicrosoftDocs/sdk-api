---
UID: NN:imapi2fs.IFileSystemImage3
title: IFileSystemImage3 (imapi2fs.h)
description: Use this interface to set or check the metadata and metadata mirror files in a UDF file system (rev 2.50 and later) to determine redundancy.
helpviewer_keywords: ["IFileSystemImage3","IFileSystemImage3 interface [IMAPI]","IFileSystemImage3 interface [IMAPI]","described","imapi.ifilesystemimage3","imapi2fs/IFileSystemImage3"]
old-location: imapi\ifilesystemimage3.htm
tech.root: imapi
ms.assetid: ffe343fa-2837-41f7-b7e0-097788fb5d4e
ms.date: 12/05/2018
ms.keywords: IFileSystemImage3, IFileSystemImage3 interface [IMAPI], IFileSystemImage3 interface [IMAPI],described, imapi.ifilesystemimage3, imapi2fs/IFileSystemImage3
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
 - IFileSystemImage3
 - imapi2fs/IFileSystemImage3
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
 - IFileSystemImage3
---

# IFileSystemImage3 interface


## -description

Use this interface to set or check the metadata and metadata mirror files in a UDF file system (rev 2.50 and later) to determine  redundancy.

## -inheritance

The <b>IFileSystemImage3</b> interface inherits from <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2">IFileSystemImage2</a>. <b>IFileSystemImage3</b> also has these types of members:

## -remarks

If the metadata and metadata mirror files are set for redundancy, IMAPI  creates identical copies of each in the file system image, which results in increased level of fault tolerance. In a scenario where the metadata files are not set for redundancy, IMAPI only creates a single copy in the file system image, which can save several MB of space on the burned disc.

The metadata redundancy option is set to <b>TRUE</b> by default.

<b>IFileSystemImage3</b> is the default interface of <b>MsftFileSystemImage3</b> objects.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<b></b>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2">IFileSystemImage2</a>
