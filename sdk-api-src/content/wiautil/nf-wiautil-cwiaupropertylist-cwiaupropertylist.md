---
UID: NF:wiautil.CWiauPropertyList.CWiauPropertyList
title: CWiauPropertyList::CWiauPropertyList method
author: windows-driver-content
description: The CWiauPropertyList::CWiauPropertyList method is the constructor for the CWiauPropertyList class.
old-location: image\cwiaupropertylist_cwiaupropertylist.htm
old-project: image
ms.assetid: 5e493d3c-81b6-4db5-a550-c86eadf5a723
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], CWiauPropertyList method, CWiauPropertyList method [Imaging Devices], CWiauPropertyList method [Imaging Devices], CWiauPropertyList interface, CWiauPropertyList,CWiauPropertyList.CWiauPropertyList, CWiauPropertyList::CWiauPropertyList, image.cwiaupropertylist_cwiaupropertylist, wiauFncs_834023ef-b425-4469-a5e7-c127fd5acf2a.xml, wiautil/CWiauPropertyList::CWiauPropertyList
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
-	CWiauPropertyList.CWiauPropertyList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::CWiauPropertyList method


## -description


The <b>CWiauPropertyList::CWiauPropertyList</b> method is the constructor for the <b>CWiauPropertyList</b> class.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <b>CWiauPropertyList</b> constructor initializes all data members of a property list object to either <b>NULL</b> or zero. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540396">CWiauPropertyList::Init</a> method to reserve memory for properties. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a> method once per property to add it to the property list object.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540396">CWiauPropertyList::Init</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540472">CWiauPropertyList::~CWiauPropertyList</a>
 

 

