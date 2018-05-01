---
UID: NF:wiamdef.wiasSetValidListStr
title: wiasSetValidListStr function
author: windows-driver-content
description: The wiasSetValidListStr function sets the valid values for a WIA_PROP_LIST property of type VT_BSTR.
old-location: image\wiassetvalidliststr.htm
old-project: image
ms.assetid: d2745d91-6696-4946-9f90-a9cb48c7980f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetvalidliststr, wiamdef/wiasSetValidListStr, wiasFncs_c18aeb74-5c44-43ea-be9e-5132f45a5f77.xml, wiasSetValidListStr, wiasSetValidListStr function [Imaging Devices]
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
-	wiasSetValidListStr
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetValidListStr function


## -description


The <b>wiasSetValidListStr </b>function sets the valid values for a WIA_PROP_LIST property of type VT_BSTR.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the identifier of the property to be updated.


### -param ulCount

Specifies the number of items in the <i>pbstrValues</i> array.


### -param bstrNom

Specifies the nominal value of the property.


### -param bstrValues

TBD




#### - pbstrValues [in]

Pointer to the first element of an array of valid property values.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549390">wiasSetValidFlag</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549399">wiasSetValidListFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549409">wiasSetValidListGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549414">wiasSetValidListLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549425">wiasSetValidRangeFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549434">wiasSetValidRangeLong</a>
 

 

