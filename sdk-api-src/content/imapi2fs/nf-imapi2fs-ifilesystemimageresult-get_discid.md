---
UID: NF:imapi2fs.IFileSystemImageResult.get_DiscId
title: IFileSystemImageResult::get_DiscId
author: windows-sdk-content
description: Retrieves the disc volume name for this file system image.
old-location: imapi\ifilesystemimageresult_get_discid.htm
tech.root: imapi
ms.assetid: 2288b4e4-6f36-4830-a077-dcf710741911
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_DiscId method, IFileSystemImageResult.get_DiscId, IFileSystemImageResult::get_DiscId, get_DiscId, get_DiscId method [IMAPI], get_DiscId method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_discid, imapi2fs/IFileSystemImageResult::get_DiscId
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImageResult.get_DiscId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IFileSystemImageResult.get_DiscId
: 
---

# IFileSystemImageResult::get_DiscId


## -description


Retrieves the disc volume name for this file system image.


## -parameters




### -param pVal [out]

String that contains the volume name for this file system image.


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




<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">IFileSystemImage::get_VolumeName</a>



<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>
 

 

