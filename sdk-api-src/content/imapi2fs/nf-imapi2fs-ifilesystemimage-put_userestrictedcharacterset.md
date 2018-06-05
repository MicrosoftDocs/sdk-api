---
UID: NF:imapi2fs.IFileSystemImage.put_UseRestrictedCharacterSet
title: IFileSystemImage::put_UseRestrictedCharacterSet
author: windows-sdk-content
description: Determines if file and directory names should be restricted to using only CP_ANSI characters.
old-location: imapi\ifilesystemimage_put_userestrictedcharacterset.htm
old-project: imapi
ms.assetid: de64ef3d-94b3-4d97-946e-8331c5a39f4b
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_UseRestrictedCharacterSet method, IFileSystemImage.put_UseRestrictedCharacterSet, IFileSystemImage::put_UseRestrictedCharacterSet, imapi.ifilesystemimage_put_userestrictedcharacterset, imapi2fs/IFileSystemImage::put_UseRestrictedCharacterSet, put_UseRestrictedCharacterSet, put_UseRestrictedCharacterSet method [IMAPI], put_UseRestrictedCharacterSet method [IMAPI],IFileSystemImage interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.put_UseRestrictedCharacterSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::put_UseRestrictedCharacterSet


## -description


Determines if file and directory names should be restricted to using only CP_ANSI characters. <div class="alert"><b>Note</b>  <b>IFileSystemImage::put_UseRestrictedCharacterSet</b> has been deprecated. Implementing this method is not recommended.</div>
<div> </div>



## -parameters




### -param newVal [in]

Set to VARIANT_TRUE to restrict file and directory names to use only CP_ANSI characters. Otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



Setting this property does not affect files or directories already in the file system image.

You can change the value of this property only when the result stream is not active.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">IFileSystemImage::CreateDirectoryItem</a>



<a href="https://msdn.microsoft.com/8e90e367-e7c3-41db-a8c9-9b0220cf402b">IFileSystemImage::CreateFileItem</a>



<a href="https://msdn.microsoft.com/106615e8-f1d4-4ac9-b96a-bcda204f5e2c">IFileSystemImage::get_UseRestrictedCharacterSet</a>
 

 

