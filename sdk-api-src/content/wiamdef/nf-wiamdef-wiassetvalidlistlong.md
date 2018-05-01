---
UID: NF:wiamdef.wiasSetValidListLong
title: wiasSetValidListLong function
author: windows-driver-content
description: The wiasSetValidListLong function sets the valid values for a WIA_PROP_LIST property of type VT_I4.
old-location: image\wiassetvalidlistlong.htm
old-project: image
ms.assetid: a8c3d2fa-7c21-4c6a-b395-af28029c9c15
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetvalidlistlong, wiamdef/wiasSetValidListLong, wiasFncs_0ccc4e24-3b86-426e-94c6-7c8bb19811f8.xml, wiasSetValidListLong, wiasSetValidListLong function [Imaging Devices]
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
-	wiasSetValidListLong
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetValidListLong function


## -description


The <b>wiasSetValidListLong </b>function sets the valid values for a WIA_PROP_LIST property of type VT_I4.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the identifier of the property to be updated.


### -param ulCount

Specifies the number of items in the <i>plValues</i> array.


### -param lNom

Specifies the property's nominal value.


### -param plValues

Pointer to the first element of an array of valid property values.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549390">wiasSetValidFlag</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549399">wiasSetValidListFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549409">wiasSetValidListGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549421">wiasSetValidListStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549425">wiasSetValidRangeFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549434">wiasSetValidRangeLong</a>
 

 

