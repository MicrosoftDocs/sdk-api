---
UID: NF:wiamdef.wiasSetValidListGuid
title: wiasSetValidListGuid function
author: windows-driver-content
description: The wiasSetValidListGuid function sets valid values for a WIA_PROP_LIST property of type VT_CLSID.
old-location: image\wiassetvalidlistguid.htm
old-project: image
ms.assetid: ab8276d4-4838-4bfc-8952-8712435eab41
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetvalidlistguid, wiamdef/wiasSetValidListGuid, wiasFncs_eade05c7-20bd-480d-aa50-0216575ce856.xml, wiasSetValidListGuid, wiasSetValidListGuid function [Imaging Devices]
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
-	wiasSetValidListGuid
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetValidListGuid function


## -description


The <b>wiasSetValidListGuid </b>function sets valid values for a WIA_PROP_LIST property of type VT_CLSID.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param propid

Specifies the identifier of the property to be updated.


### -param ulCount

Specifies the number of items in the <i>pgValues</i> array.


### -param guidNom

TBD


### -param pguidValues

TBD




#### - gNom

Specifies the property's nominal value.


#### - pgValues [in]

Pointer to the first element of an array of valid property values.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549390">wiasSetValidFlag</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549399">wiasSetValidListFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549414">wiasSetValidListLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549421">wiasSetValidListStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549425">wiasSetValidRangeFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549434">wiasSetValidRangeLong</a>
 

 

