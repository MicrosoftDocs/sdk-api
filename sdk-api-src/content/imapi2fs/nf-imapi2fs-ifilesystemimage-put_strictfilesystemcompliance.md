---
UID: NF:imapi2fs.IFileSystemImage.put_StrictFileSystemCompliance
title: IFileSystemImage::put_StrictFileSystemCompliance
author: windows-sdk-content
description: Determines the compliance level for creating and developing the file-system image.
old-location: imapi\ifilesystemimage_put_strictfilesystemcompliance.htm
old-project: imapi
ms.assetid: ccbeba5a-39d5-43fd-8693-fee7cbbf5c8a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_StrictFileSystemCompliance method, IFileSystemImage.put_StrictFileSystemCompliance, IFileSystemImage::put_StrictFileSystemCompliance, imapi.ifilesystemimage_put_strictfilesystemcompliance, imapi2fs/IFileSystemImage::put_StrictFileSystemCompliance, put_StrictFileSystemCompliance, put_StrictFileSystemCompliance method [IMAPI], put_StrictFileSystemCompliance method [IMAPI],IFileSystemImage interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.put_StrictFileSystemCompliance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::put_StrictFileSystemCompliance


## -description


Determines the compliance level for creating and developing the file-system image.


## -parameters




### -param newVal [in]

Set to VARIANT_TRUE to create the file system images in strict compliance with applicable standards.  You can specify VARIANT_TRUE only when the file system image is empty.

Set to VARIANT_FALSE to relax the compliance standards to be compatible with IMAPI version 1.0.

The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



If this property is VARIANT_TRUE and a method requests an action that violates one of the file system constraints, an exception is thrown.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/07139ef3-ffd5-4035-afa9-6212808a6fbc">IFileSystemImage::get_StrictFileSystemCompliance</a>
 

 

