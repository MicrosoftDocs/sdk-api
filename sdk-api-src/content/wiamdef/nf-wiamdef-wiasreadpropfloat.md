---
UID: NF:wiamdef.wiasReadPropFloat
title: wiasReadPropFloat function
author: windows-driver-content
description: The wiasReadPropFloat function retrieves a floating-point property value from a WIA item.
old-location: image\wiasreadpropfloat.htm
old-project: image
ms.assetid: 042ef9d9-a980-41eb-a396-e03658ea072a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasreadpropfloat, wiamdef/wiasReadPropFloat, wiasFncs_9b143e96-64a5-4de3-b40d-c542bc440dc0.xml, wiasReadPropFloat, wiasReadPropFloat function [Imaging Devices]
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
-	wiasReadPropFloat
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasReadPropFloat function


## -description


The <b>wiasReadPropFloat </b>function retrieves a floating-point property value from a WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the property identifier.


### -param pfVal [out]

Pointer to a memory location that receives the floating-point value of the property.


### -param pfValOld [out, optional]

Pointer to a memory location that receives the former floating-point value of the property. If this information is not needed, set this parameter to <b>NULL</b>.


### -param bMustExist

Indicates whether the property must exist. If set to <b>TRUE</b>, the property must exist; if set to <b>FALSE</b>, it does not have to exist.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549308">wiasReadPropBin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549325">wiasReadPropGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549330">wiasReadPropLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549341">wiasReadPropStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549507">wiasWritePropFloat</a>
 

 

