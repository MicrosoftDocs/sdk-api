---
UID: NF:wiamdef.wiasReadMultiple
title: wiasReadMultiple function
author: windows-driver-content
description: The wiasReadMultiple function retrieves multiple property values from a WIA item.
old-location: image\wiasreadmultiple.htm
old-project: image
ms.assetid: 814642f7-24df-4d64-bc2b-d76d84b2a6d3
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasreadmultiple, wiamdef/wiasReadMultiple, wiasFncs_c6d42143-4cd8-4f9a-bbf4-aec0ce2c0615.xml, wiasReadMultiple, wiasReadMultiple function [Imaging Devices]
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
-	wiasReadMultiple
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasReadMultiple function


## -description


The <b>wiasReadMultiple </b>function retrieves multiple property values from a WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param ulCount

Specifies the number of properties to read.


### -param ps [in]

Pointer to the first element of an array of PROPSPEC structures, containing the properties to read.


### -param pv [out]

Pointer to the first element of an array of PROPVARIANT structures. Upon return, these structures contain new values for the properties.


### -param pvOld [out, optional]

Pointer to the first element of an array of PROPVARIANT structures previously allocated by the minidriver. Upon return, the array contains the previous values of the property data. If this information is not needed, this parameter can be set to <b>NULL</b>.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



This function reads multiple properties from a WIA item. When the call succeeds, the minidriver must call <b>PropVariantClear</b> on each element in the array specified by the <i>pv</i> parameter. See <b>IPropertyStorage::ReadMultiple</b> for more information.

PROPSPEC, PROPVARIANT, <b>PropVariantClear</b>, and <b>IPropertyStorage::ReadMultiple</b> are described in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549475">wiasWriteMultiple</a>
 

 

