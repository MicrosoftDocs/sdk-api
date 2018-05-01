---
UID: NF:wiamdef.wiasWriteBufToFile
title: wiasWriteBufToFile function
author: windows-driver-content
description: The wiasWriteBufToFile function writes from a specified buffer to an image file.
old-location: image\wiaswritebuftofile.htm
old-project: image
ms.assetid: 29e9fa32-9264-41d7-8ac2-c6a08cab2880
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaswritebuftofile, wiamdef/wiasWriteBufToFile, wiasFncs_9d14f2bd-ceba-491a-808c-9af7cdcc8b6b.xml, wiasWriteBufToFile, wiasWriteBufToFile function [Imaging Devices]
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
-	wiasWriteBufToFile
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasWriteBufToFile function


## -description


The <b>wiasWriteBufToFile</b> function writes from a specified buffer to an image file.


## -parameters




### -param lFlags

Specifies a set of operation flags. This parameter should be set to 0.


### -param pmdtc [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



A WIA minidriver uses this function to write a buffer to any type of image file. A driver that intends to write a page of purely image data to a multipage TIFF file, delegating the addition of the appropriate tags, image file directory (IFD) entries, and other nonimage data to the WIA service, should use <a href="https://msdn.microsoft.com/library/windows/hardware/ff549484">wiasWritePageBufToFile</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549484">wiasWritePageBufToFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549495">wiasWritePageBufToStream</a>
 

 

