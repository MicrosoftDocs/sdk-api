---
UID: NF:wiamdef.wiasSetValidRangeFloat
title: wiasSetValidRangeFloat function
author: windows-driver-content
description: The wiasSetValidRangeFloat function specifies the range of valid values for a WIA_PROP_RANGE property of type VT_R4.
old-location: image\wiassetvalidrangefloat.htm
old-project: image
ms.assetid: 66bc5e03-4cc2-4de3-b707-18ff7e0deb4b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetvalidrangefloat, wiamdef/wiasSetValidRangeFloat, wiasFncs_d8eb35e4-e295-43cf-a457-5e6fac3f537d.xml, wiasSetValidRangeFloat, wiasSetValidRangeFloat function [Imaging Devices]
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
-	wiasSetValidRangeFloat
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetValidRangeFloat function


## -description


The <b>wiasSetValidRangeFloat </b>function specifies the range of valid values for a WIA_PROP_RANGE property of type VT_R4.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the identifier of the property to be updated.


### -param fMin

Specifies the minimum value of the valid range.


### -param fNom

Specifies the property's nominal value.


### -param fMax

Specifies the maximum value of the valid range.


### -param fStep

Specifies the increment between each valid value in the range.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549390">wiasSetValidFlag</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549399">wiasSetValidListFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549409">wiasSetValidListGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549414">wiasSetValidListLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549421">wiasSetValidListStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549434">wiasSetValidRangeLong</a>
 

 

