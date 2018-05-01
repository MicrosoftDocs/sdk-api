---
UID: NF:wiamdef.wiasSetPropChanged
title: wiasSetPropChanged function
author: windows-driver-content
description: The wiasSetPropChanged function modifies a property context to indicate that a property is being changed.
old-location: image\wiassetpropchanged.htm
old-project: image
ms.assetid: f17f6935-02ad-44f4-a82a-0d51802fde6f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetpropchanged, wiamdef/wiasSetPropChanged, wiasFncs_8ad54c6e-3a20-4099-a139-1a05f6ee1e5e.xml, wiasSetPropChanged, wiasSetPropChanged function [Imaging Devices]
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
-	wiasSetPropChanged
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetPropChanged function


## -description


The <b>wiasSetPropChanged </b>function modifies a property context to indicate that a property is being changed.


## -parameters




### -param propid

Specifies the property identifier of the property being changed.


### -param pContext [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a> structure that contains the current property context.


### -param bChanged

Specifies the BOOL value that is used to set a particular element in the array pointed to by the <b>pChanged</b> member of a WIA_PROPERTY_CONTEXT structure. See the <b>Remarks</b> section for more details.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



The <b>pChanged</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a> structure points to an array of BOOL values that indicate whether a particular property will be changed. This function sets one element in that array for the specified property in the property context. This function should be used whenever a driver changes a property that has dependent properties in validation. For example, by changing "Current Intent", the "Horizontal Resolution" is changed and should be marked as changed, so that validation of "X Resolution" (<a href="https://msdn.microsoft.com/library/windows/hardware/ff552665">WIA_IPS_XRES</a>)and its dependents still takes place.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552749">WIA_PROPERTY_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549271">wiasIsPropChanged</a>
 

 

