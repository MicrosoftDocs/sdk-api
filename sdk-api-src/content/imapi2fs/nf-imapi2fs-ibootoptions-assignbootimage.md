---
UID: NF:imapi2fs.IBootOptions.AssignBootImage
title: IBootOptions::AssignBootImage
author: windows-sdk-content
description: Sets the data stream that contains the boot image.
old-location: imapi\ibootoptions_assignbootimage.htm
tech.root: imapi
ms.assetid: 63d598dd-72a8-4544-813d-11f2e7e53ec5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AssignBootImage, AssignBootImage method [IMAPI], AssignBootImage method [IMAPI],IBootOptions interface, IBootOptions interface [IMAPI],AssignBootImage method, IBootOptions.AssignBootImage, IBootOptions::AssignBootImage, imapi.ibootoptions_assignbootimage, imapi2fs/IBootOptions::AssignBootImage
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
 - IBootOptions.AssignBootImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootOptions::AssignBootImage


## -description


Sets the data stream that contains the boot image.


## -parameters




### -param newVal [in]

An <b>IStream</b> interface of the data stream that contains the boot image.


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
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_IMAGE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The boot object could not be added to the image.

Value: 0xC0AAB142

</td>
</tr>
</table>
 




## -remarks



If the size of the newly assigned boot image is either 1.2, 1.44. or 2.88 MB, this method will automatically adjust the <a href="https://msdn.microsoft.com/53e87d6d-9547-4437-9548-652cfcbd308e">EmulationType</a> value to the respective "floppy" type value.   It is, however, possible to  override the default or previously assigned <b>EmulationType</b> value by calling the <a href="https://msdn.microsoft.com/93ed301e-fdea-451c-9ab0-6ea9a7fd45de">IBootOptions::put_Emulation</a> method.

The additional specification of the platform on which to use the boot image requires the call to the <a href="https://msdn.microsoft.com/295f3a3c-0f01-4b9b-b73c-48f075e6a33a">IBootOptions::put_PlatformId</a> method.

IMAPI does not include any boot images; developers must provide their own boot images.




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/161e0cea-63dd-4806-a246-4b36249b2cc7">IBootOptions::get_BootImage</a>



<a href="https://msdn.microsoft.com/b9721313-a2b0-4d91-af10-7932bd2d01be">IFileSystemImage::get_BootImageOptions</a>



<a href="https://msdn.microsoft.com/0556b72d-eabd-4649-b16b-fd66052504f4">IFileSystemImage::put_BootImageOptions</a>
 

 

