---
UID: NF:imapi2fs.IFileSystemImage.get_ISO9660InterchangeLevel
title: IFileSystemImage::get_ISO9660InterchangeLevel method
author: windows-driver-content
description: Retrieves the ISO9660 compatibility level to use when creating the result image.
old-location: imapi\ifilesystemimage_get_iso9660interchangelevel.htm
old-project: imapi
ms.assetid: 9536444b-60e4-456f-b6d8-07cf9a6f7848
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IFileSystemImage, IFileSystemImage interface [IMAPI], get_ISO9660InterchangeLevel method, IFileSystemImage::get_ISO9660InterchangeLevel, get_ISO9660InterchangeLevel method [IMAPI], get_ISO9660InterchangeLevel method [IMAPI], IFileSystemImage interface, get_ISO9660InterchangeLevel,IFileSystemImage.get_ISO9660InterchangeLevel, imapi.ifilesystemimage_get_iso9660interchangelevel, imapi2fs/IFileSystemImage::get_ISO9660InterchangeLevel
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IFileSystemImage.get_ISO9660InterchangeLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::get_ISO9660InterchangeLevel method


## -description


Retrieves the ISO9660 compatibility level to use when creating the result image.


## -parameters




### -param pVal [out]

Identifies the interchange level of the ISO9660 file system. 


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



For a list of supported compatibility levels, call the <a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f">IFileSystemImage::get_ISO9660InterchangeLevelsSupported</a>



<a href="https://msdn.microsoft.com/8bfb770a-5a69-4980-94e2-4a3f65caa645">IFileSystemImage::put_ISO9660InterchangeLevel</a>
 

 

