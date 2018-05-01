---
UID: NF:wiamdef.wiasGetDrvItem
title: wiasGetDrvItem function
author: windows-driver-content
description: The wiasGetDrvItem function retrieves a driver item.
old-location: image\wiasgetdrvitem.htm
old-project: image
ms.assetid: c09924ef-cd2c-419c-81d5-bbd40b886767
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetdrvitem, wiamdef/wiasGetDrvItem, wiasFncs_47e70917-9675-4291-a76a-46aa734efef3.xml, wiasGetDrvItem, wiasGetDrvItem function [Imaging Devices]
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
-	wiasGetDrvItem
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetDrvItem function


## -description


The <b>wiasGetDrvItem </b>function retrieves a driver item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param ppIWiaDrvItem

TBD




#### - ppDrvItem [out]

Pointer to a memory location that receives the address of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff543896">IWiaDrvItem Interface</a>.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549264">wiasGetRootItem</a>
 

 

