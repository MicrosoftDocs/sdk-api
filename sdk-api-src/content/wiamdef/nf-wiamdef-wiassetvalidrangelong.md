---
UID: NF:wiamdef.wiasSetValidRangeLong
title: wiasSetValidRangeLong function
author: windows-driver-content
description: The wiasSetValidRangeLong function specifies the range of valid values for a WIA_PROP_RANGE property of type VT_I4.
old-location: image\wiassetvalidrangelong.htm
old-project: image
ms.assetid: ff4badb5-ab27-4deb-864a-51165290bca4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetvalidrangelong, wiamdef/wiasSetValidRangeLong, wiasFncs_3ee53b59-4ef4-4c35-8544-1ac7a8729212.xml, wiasSetValidRangeLong, wiasSetValidRangeLong function [Imaging Devices]
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
-	wiasSetValidRangeLong
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetValidRangeLong function


## -description


The <b>wiasSetValidRangeLong </b>function specifies the range of valid values for a WIA_PROP_RANGE property of type VT_I4.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the identifier of the property to be updated.


### -param lMin

Specifies the minimum value of the valid range.


### -param lNom

Specifies the property's nominal value.


### -param lMax

Specifies the maximum value of the valid range.


### -param lStep

Specifies the increment between each valid value in the range.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549390">wiasSetValidFlag</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549399">wiasSetValidListFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549409">wiasSetValidListGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549414">wiasSetValidListLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549421">wiasSetValidListStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549425">wiasSetValidRangeFloat</a>
 

 

