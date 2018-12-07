---
UID: NF:imapi2fs.IBootOptions.get_BootImage
title: IBootOptions::get_BootImage
author: windows-sdk-content
description: Retrieves a pointer to the boot image data stream.
old-location: imapi\ibootoptions_get_bootimage.htm
tech.root: imapi
ms.assetid: 161e0cea-63dd-4806-a246-4b36249b2cc7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBootOptions interface [IMAPI],get_BootImage method, IBootOptions.get_BootImage, IBootOptions::get_BootImage, get_BootImage, get_BootImage method [IMAPI], get_BootImage method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_bootimage, imapi2fs/IBootOptions::get_BootImage
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
 - IBootOptions.get_BootImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootOptions::get_BootImage


## -description


Retrieves a pointer to the boot image data stream.


## -parameters




### -param pVal [out]

Pointer to the <b>IStream</b> interface associated with the boot image data stream.


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




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/63d598dd-72a8-4544-813d-11f2e7e53ec5">IBootOptions::AssignBootImage</a>



<a href="https://msdn.microsoft.com/b9721313-a2b0-4d91-af10-7932bd2d01be">IFileSystemImage::get_BootImageOptions</a>



<a href="https://msdn.microsoft.com/0556b72d-eabd-4649-b16b-fd66052504f4">IFileSystemImage::put_BootImageOptions</a>
 

 

