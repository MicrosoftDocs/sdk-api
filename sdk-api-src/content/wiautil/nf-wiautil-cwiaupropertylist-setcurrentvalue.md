---
UID: NF:wiautil.CWiauPropertyList.SetCurrentValue
title: CWiauPropertyList::SetCurrentValue method
author: windows-driver-content
description: The CWiauPropertyList::SetCurrentValue(BSTR) method sets the current value of a property of type BSTR, and sets its type to VT_BSTR.
old-location: image\cwiaupropertylist_setcurrentvalue_bstr_.htm
old-project: image
ms.assetid: 017ab648-ee62-47f5-abd3-f4eac4378b8a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], SetCurrentValue method, CWiauPropertyList::SetCurrentValue, SetCurrentValue method [Imaging Devices], SetCurrentValue method [Imaging Devices], CWiauPropertyList interface, SetCurrentValue,CWiauPropertyList.SetCurrentValue, image.cwiaupropertylist_setcurrentvalue_bstr_, wiauFncs_dfd640f7-63c2-41a6-adf3-589e87aa85cc.xml, wiautil/CWiauPropertyList::SetCurrentValue
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
-	CWiauPropertyList.SetCurrentValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::SetCurrentValue method


## -description


The <b>CWiauPropertyList::SetCurrentValue(BSTR)</b> method sets the current value of a property of type <b>BSTR</b>, and sets its type to VT_BSTR.


## -parameters




### -param index

Specifies the property index. Set this parameter to the value in *<i>pIdx</i> when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a> method returns.


### -param value

Pointer to a memory location containing the value that is written to the device property in the property list. This pointer must remain valid until the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540403">CWiauPropertyList::SendToWia</a> method is called.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540403">CWiauPropertyList::SendToWia</a>
 

 

