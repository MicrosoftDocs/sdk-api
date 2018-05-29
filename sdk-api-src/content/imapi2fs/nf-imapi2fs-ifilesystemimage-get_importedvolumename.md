---
UID: NF:imapi2fs.IFileSystemImage.get_ImportedVolumeName
title: IFileSystemImage::get_ImportedVolumeName
author: windows-sdk-content
description: Retrieves the volume name provided from an imported file system.
old-location: imapi\ifilesystemimage_get_importedvolumename.htm
old-project: imapi
ms.assetid: 57d66dd3-2525-4102-bba7-00bad76a3d9c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_ImportedVolumeName method, IFileSystemImage.get_ImportedVolumeName, IFileSystemImage::get_ImportedVolumeName, get_ImportedVolumeName, get_ImportedVolumeName method [IMAPI], get_ImportedVolumeName method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_importedvolumename, imapi2fs/IFileSystemImage::get_ImportedVolumeName
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFileSystemImage.get_ImportedVolumeName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_ImportedVolumeName


## -description


Retrieves the volume name provided from an imported file system.  


## -parameters




### -param pVal [out]

String that contains the volume name provided from an imported file system. Is <b>NULL</b> until a file system is imported.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



The imported volume name is provided for user information and is not automatically carried forward to subsequent sessions.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">IFileSystemImage::get_VolumeName</a>



<a href="https://msdn.microsoft.com/afb87eb1-5d14-413a-8830-2612920eac3d">IFileSystemImage::put_VolumeName</a>
 

 

