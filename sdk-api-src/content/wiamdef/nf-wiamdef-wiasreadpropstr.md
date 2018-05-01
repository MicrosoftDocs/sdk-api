---
UID: NF:wiamdef.wiasReadPropStr
title: wiasReadPropStr function
author: windows-driver-content
description: The wiasReadPropStr function retrieves a string property value from a WIA item.
old-location: image\wiasreadpropstr.htm
old-project: image
ms.assetid: b072b4ec-790f-454b-b94a-bfe44674f600
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasreadpropstr, wiamdef/wiasReadPropStr, wiasFncs_b0756dcf-44dd-4a9f-ad9a-1edff1b8e6f6.xml, wiasReadPropStr, wiasReadPropStr function [Imaging Devices]
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
-	wiasReadPropStr
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasReadPropStr function


## -description


The <b>wiasReadPropStr</b> function retrieves a string property value from a WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the property identifier.


### -param pbstr [out]

Pointer to a memory location that receives the first byte of the property's string value.


### -param pbstrOld [out, optional]

Pointer to a memory location that receives the first byte of the property's previous value. If this information is not needed, set this parameter to <b>NULL</b>.


### -param bMustExist

Indicates whether the property must exist. If set to <b>TRUE</b>, the property must exist; if set to <b>FALSE</b>, the property does not have to exist.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



When the minidriver has completed using the string it received from this function, it must deallocate the memory used for the string.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549308">wiasReadPropBin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549320">wiasReadPropFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549325">wiasReadPropGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549330">wiasReadPropLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549525">wiasWritePropStr</a>
 

 

