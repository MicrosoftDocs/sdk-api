---
UID: NF:imapi2fs.IFileSystemImage.get_VolumeNameUDF
title: IFileSystemImage::get_VolumeNameUDF
author: windows-sdk-content
description: Retrieves the volume name for the UDF system image.
old-location: imapi\ifilesystemimage_get_volumenameudf.htm
old-project: imapi
ms.assetid: d034f8cb-38f5-42ab-8952-e4a76dc1f27d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_VolumeNameUDF method, IFileSystemImage.get_VolumeNameUDF, IFileSystemImage::get_VolumeNameUDF, get_VolumeNameUDF, get_VolumeNameUDF method [IMAPI], get_VolumeNameUDF method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_volumenameudf, imapi2fs/IFileSystemImage::get_VolumeNameUDF
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.get_VolumeNameUDF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_VolumeNameUDF


## -description


Retrieves the volume name for the UDF system image.


## -parameters




### -param pVal [out]

String that contains the volume name for the UDF system image.


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
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">IFileSystemImage::get_VolumeName</a>



<a href="https://msdn.microsoft.com/9f41c273-d56a-4e8f-aa9f-e2a49741f7e3">IFileSystemImage::get_VolumeNameISO9660</a>



<a href="https://msdn.microsoft.com/5300763d-9f2f-4562-bb5e-61fcf485b086">IFileSystemImage::get_VolumeNameJoliet</a>
 

 

