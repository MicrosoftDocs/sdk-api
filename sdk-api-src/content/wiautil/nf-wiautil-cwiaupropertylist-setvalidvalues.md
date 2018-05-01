---
UID: NF:wiautil.CWiauPropertyList.SetValidValues
title: CWiauPropertyList::SetValidValues method
author: windows-driver-content
description: The CWiauPropertyList::SetValidValues(BSTR, list) method sets the type, as well as default, current, and valid values for a BSTR property associated with a list of values.
old-location: image\cwiaupropertylist_setvalidvalues_bstr__list_.htm
old-project: image
ms.assetid: b806e310-4e6d-4258-8dd5-0c9aa35a35f4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], SetValidValues method, CWiauPropertyList::SetValidValues, SetValidValues method [Imaging Devices], SetValidValues method [Imaging Devices], CWiauPropertyList interface, SetValidValues,CWiauPropertyList.SetValidValues, image.cwiaupropertylist_setvalidvalues_bstr__list_, wiauFncs_7653406d-852f-452e-94c3-187be530f684.xml, wiautil/CWiauPropertyList::SetValidValues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiautil.h
req.include-header: Wiautil.h, Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiautil.h
api_name:
-	CWiauPropertyList.SetValidValues
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::SetValidValues method


## -description


The <b>CWiauPropertyList::SetValidValues(BSTR, list)</b> method sets the type, as well as default, current, and valid values for a <b>BSTR</b> property associated with a list of values. The method also sets the property type to VT_BSTR and subtype to WIA_PROP_LIST (defined in the Microsoft Windows SDK documentation).


## -parameters




### -param index

Specifies the property index. Set this parameter to the value in *<i>pIdx</i> when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a> method returns.


### -param defaultValue

Specifies the default setting of the property on the device.


### -param currentValue

Specifies the current setting of the property on the device.


### -param validFlags






#### - numValues

Specifies the number of values in the property list.


#### - pValues

Points to the first property in the property list. This pointer must remain valid until the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540403">CWiauPropertyList::SendToWia</a> method is called.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540403">CWiauPropertyList::SendToWia</a>
 

 

