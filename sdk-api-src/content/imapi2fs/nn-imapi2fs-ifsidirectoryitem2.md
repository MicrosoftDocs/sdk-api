---
UID: NN:imapi2fs.IFsiDirectoryItem2
title: IFsiDirectoryItem2 (imapi2fs.h)
description: Use this interface to add a directory tree, which includes all sub-directories, files, and associated named streams to a file system image.
helpviewer_keywords: ["IFsiDirectoryItem2","IFsiDirectoryItem2 interface [IMAPI]","IFsiDirectoryItem2 interface [IMAPI]","described","imapi.ifsidirectoryitem2","imapi2fs/IFsiDirectoryItem2"]
old-location: imapi\ifsidirectoryitem2.htm
tech.root: imapi
ms.assetid: fed2a858-d710-46be-a05b-dce7ef484636
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem2, IFsiDirectoryItem2 interface [IMAPI], IFsiDirectoryItem2 interface [IMAPI],described, imapi.ifsidirectoryitem2, imapi2fs/IFsiDirectoryItem2
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
 - IFsiDirectoryItem2
 - imapi2fs/IFsiDirectoryItem2
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
 - IFsiDirectoryItem2
---

# IFsiDirectoryItem2 interface


## -description

Use this interface to add a directory tree, which includes all sub-directories, files, and associated named streams to a file system image.

## -inheritance

The <b>IFsiDirectoryItem2</b> interface inherits from <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>. <b>IFsiDirectoryItem2</b> also has these types of members:

## -remarks

All sub-directories, files, and associated named streams can only be added after the directory item has been  added to the file system image.

UDF must be enabled and set to UDF revision 2.00 or later in order to enable named stream support during the creation of the file system image.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<b></b>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>
