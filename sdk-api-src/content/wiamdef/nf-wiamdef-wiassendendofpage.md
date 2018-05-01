---
UID: NF:wiamdef.wiasSendEndOfPage
title: wiasSendEndOfPage function
author: windows-driver-content
description: The wiasSendEndOfPage function calls the client callback routine during a data transfer, sending the current total page count.
old-location: image\wiassendendofpage.htm
old-project: image
ms.assetid: 107cd468-bc39-4672-9356-e5329b36277b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassendendofpage, wiamdef/wiasSendEndOfPage, wiasFncs_c8a81130-c832-40d8-8a62-619d04d8d3dc.xml, wiasSendEndOfPage, wiasSendEndOfPage function [Imaging Devices]
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
-	wiasSendEndOfPage
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSendEndOfPage function


## -description


The <b>wiasSendEndOfPage </b>function calls the client callback routine during a data transfer, sending the current total page count.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param lPageCount

Specifies the total page count. 


### -param pmdtc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>
 

 

