---
UID: NF:imapi2fs.IFileSystemImage2.get_BootImageOptionsArray
title: IFileSystemImage2::get_BootImageOptionsArray
author: windows-driver-content
description: Retrieves the boot option array that will be utilized to generate the file system image.
old-location: imapi\ifilesystemimage2_get_bootimageoptionsarray.htm
old-project: imapi
ms.assetid: 31e4c8e8-7a00-41e7-b3cf-78dbc10fc3d2
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFileSystemImage2 interface [IMAPI],get_BootImageOptionsArray method, IFileSystemImage2.get_BootImageOptionsArray, IFileSystemImage2::get_BootImageOptionsArray, get_BootImageOptionsArray, get_BootImageOptionsArray method [IMAPI], get_BootImageOptionsArray method [IMAPI],IFileSystemImage2 interface, imapi.ifilesystemimage2_get_bootimageoptionsarray, imapi2fs/IFileSystemImage2::get_BootImageOptionsArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	IFileSystemImage2.get_BootImageOptionsArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage2::get_BootImageOptionsArray


## -description


Retrieves the boot option array that will be utilized to generate the file system image.


## -parameters




### -param pVal [out]

Pointer to a boot option array that contains a list of <a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a> interfaces of boot images used to generate the file system image. Each element of the list is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>.


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



 The <b>SAFEARRAY</b> will be a one-dimensional array. If a boot image is not specified, a zero-sized array will be returned.




## -see-also




<a href="https://msdn.microsoft.com/c38995b7-6f32-4489-bb6c-0e3561b11f81">IFileSystemImage2</a>



<a href="https://msdn.microsoft.com/0b827f6a-8e40-4d9d-bec6-8d7f33dade43">IFileSystemImage2::put_BootImageOptionsArray</a>
 

 

