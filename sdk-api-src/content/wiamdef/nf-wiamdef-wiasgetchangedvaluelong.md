---
UID: NF:wiamdef.wiasGetChangedValueLong
title: wiasGetChangedValueLong function
author: windows-driver-content
description: The wiasGetChangedValueLong function determines whether a property with a long integer value has been changed by an application.
old-location: image\wiasgetchangedvaluelong.htm
old-project: image
ms.assetid: 2c23729c-9fab-4e3c-9205-175a6aba8f8a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetchangedvaluelong, wiamdef/wiasGetChangedValueLong, wiasFncs_c333720c-e0e9-4fa4-9fdc-24a6a248f58b.xml, wiasGetChangedValueLong, wiasGetChangedValueLong function [Imaging Devices]
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
-	wiasGetChangedValueLong
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetChangedValueLong function


## -description


The <b>wiasGetChangedValueLong </b>function determines whether a property with a long integer value has been changed by an application.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param pContext [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a> structure that contains the current property context.


### -param bNoValidation

Indicates whether the property's current value should be validated against its set of valid values. If this parameter is set to <b>TRUE</b>, the function does not perform validation on the property. If it is <b>FALSE</b>, the function performs data validation. 


### -param propID

Specifies the property identifier of the property being tested.


### -param pInfo

TBD




#### - pValInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549535">WIAS_CHANGED_VALUE_INFO</a> structure that contains the current and previous values of the property.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



The driver should validate the property only after the driver has updated the values of the property. The driver updates the values as a result of property changes requested by the application.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549535">WIAS_CHANGED_VALUE_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549200">wiasGetChangedValueFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549211">wiasGetChangedValueGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549219">wiasGetChangedValueStr</a>
 

 

