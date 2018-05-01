---
UID: NF:wiamdef.wiasGetImageInformation
title: wiasGetImageInformation function
author: windows-driver-content
description: The wiasGetImageInformation function retrieves transfer context information from an item.
old-location: image\wiasgetimageinformation.htm
old-project: image
ms.assetid: 457c4b98-313d-4b31-aa6c-fb62fea6fc7d
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetimageinformation, wiamdef/wiasGetImageInformation, wiasFncs_6603ae74-b0b9-48f4-9fa9-83cdf3edc1d6.xml, wiasGetImageInformation, wiasGetImageInformation function [Imaging Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasGetImageInformation
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetImageInformation function


## -description


The <b>wiasGetImageInformation </b>function retrieves transfer context information from an item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param lFlags

Specifies operational flags. Currently, only the following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WIAS_INIT_CONTEXT

</td>
<td>
Initialize the MINIDRV_TRANSFER_CONTEXT structure.

</td>
</tr>
</table>
 


### -param pmdtc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure. Upon return, this structure contains the requested image item information.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



This function uses a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure to calculate item image and item header sizes. In addition, it can optionally fill in an image header if the image format requires a data header. The header will be copied to the buffer if the <b>pTransferBuffer</b> member of the MINIDRV_TRANSFER_CONTEXT structure is not <b>NULL</b>. When using image formats (such as JPEG) that do not have a header, the header size in the <b>lHeaderSize</b> member of the MINIDRV_TRANSFER_CONTEXT structure is reported as zero.

For image formats where the actual final size of the image is not known until after data acquisition, as with multipage TIFF and compressed formats, the <b>lItemSize</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure is reported as zero. The <b>lImageSize</b> member is reported as the size, in bytes, of the uncompressed image in a single page. 

If WIAS_INIT_CONTEXT is specified in the <i>lFlags</i> parameter, the MINIDRV_TRANSFER_CONTEXT structure pointed to by the <i>pmdtc</i> parameter is filled in with information derived from the item's image properties. This flag should be used when a minidriver has allocated a new context.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>
 

 

