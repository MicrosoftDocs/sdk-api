---
UID: NF:imapi2fs.IFileSystemImage.put_BootImageOptions
title: IFileSystemImage::put_BootImageOptions
author: windows-sdk-content
description: Sets the boot image that you want to add to the file-system image. This method creates a complete copy of the passed-in boot options by copying the stream from the supplied IBootOptions interface.
old-location: imapi\ifilesystemimage_put_bootimageoptions.htm
tech.root: imapi
ms.assetid: 0556b72d-eabd-4649-b16b-fd66052504f4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_BootImageOptions method, IFileSystemImage.put_BootImageOptions, IFileSystemImage::put_BootImageOptions, imapi.ifilesystemimage_put_bootimageoptions, imapi2fs/IFileSystemImage::put_BootImageOptions, put_BootImageOptions, put_BootImageOptions method [IMAPI], put_BootImageOptions method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage.put_BootImageOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::put_BootImageOptions


## -description


Sets the boot image that you want to add to the file-system image. This method creates a complete copy of the passed-in boot options by copying the stream from the supplied <a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a> interface.


## -parameters




### -param newVal [in]

An <a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a> interface of the boot image that you want to add to the file-system image. Can be <b>NULL</b>.


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
<dt><b>IMAPI_E_BOOT_OBJECT_CONFLICT</b></dt>
</dl>
</td>
<td width="60%">
A boot object can only be included in an initial disc image.

Value: 0xC0AAB149

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_IMAGE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The boot object could not be added to the image.

Value: 0xC0AAB148

</td>
</tr>
</table>
 




## -remarks



You can specify a boot image only if the file system image has no previous sessions. The boot image must start at the first sector of the disc.




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/b9721313-a2b0-4d91-af10-7932bd2d01be">IFileSystemImage::get_BootImageOptions</a>
 

 

