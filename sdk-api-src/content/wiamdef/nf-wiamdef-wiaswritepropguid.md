---
UID: NF:wiamdef.wiasWritePropGuid
title: wiasWritePropGuid function
author: windows-driver-content
description: The wiasWritePropGuid function writes a single GUID property value to a WIA item.
old-location: image\wiaswritepropguid.htm
old-project: image
ms.assetid: 1189fe8d-7b94-46ed-9090-bfe40f244e6a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaswritepropguid, wiamdef/wiasWritePropGuid, wiasFncs_2d4110e9-d2e5-47a2-8213-d221e77c527d.xml, wiasWritePropGuid, wiasWritePropGuid function [Imaging Devices]
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
-	wiasWritePropGuid
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasWritePropGuid function


## -description


The <b>wiasWritePropGuid </b>function writes a single GUID property value to a WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the property identifier.


### -param guidVal

TBD




#### - gVal

Specifies a GUID property value to write to the item.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549325">wiasReadPropGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549500">wiasWritePropBin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549507">wiasWritePropFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549515">wiasWritePropLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549525">wiasWritePropStr</a>
 

 

