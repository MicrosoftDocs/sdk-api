---
UID: NF:wiamdef.wiasWritePropLong
title: wiasWritePropLong function
author: windows-driver-content
description: The wiasWritePropLong function writes a single long integer property value to a WIA item.
old-location: image\wiaswriteproplong.htm
old-project: image
ms.assetid: bc7122e4-acba-4115-98c8-ccb71b71e2c0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaswriteproplong, wiamdef/wiasWritePropLong, wiasFncs_af342c9b-5f61-492d-9765-86d62d492b55.xml, wiasWritePropLong, wiasWritePropLong function [Imaging Devices]
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
-	wiasWritePropLong
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasWritePropLong function


## -description


The <b>wiasWritePropLong </b>function writes a single long integer property value to a WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the property identifier.


### -param lVal

Specifies the long integer property value to write to the item.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549330">wiasReadPropLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549500">wiasWritePropBin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549507">wiasWritePropFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549512">wiasWritePropGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549525">wiasWritePropStr</a>
 

 

