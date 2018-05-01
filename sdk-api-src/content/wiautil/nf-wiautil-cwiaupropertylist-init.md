---
UID: NF:wiautil.CWiauPropertyList.Init
title: CWiauPropertyList::Init method
author: windows-driver-content
description: The CWiauPropertyList::Init method initializes a property list object.
old-location: image\cwiaupropertylist_init.htm
old-project: image
ms.assetid: cbbe0d76-7fd1-4653-ad79-d5e6d692dec0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], Init method, CWiauPropertyList::Init, Init method [Imaging Devices], Init method [Imaging Devices], CWiauPropertyList interface, Init,CWiauPropertyList.Init, image.cwiaupropertylist_init, wiauFncs_4bc30663-6fd6-45b7-a18f-1adc766489be.xml, wiautil/CWiauPropertyList::Init
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
-	CWiauPropertyList.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::Init method


## -description


The <b>CWiauPropertyList::Init</b> method initializes a property list object.


## -parameters




### -param NumProps

Specifies the number of properties within the property list for which to reserve space. This number can be larger than the actual number of properties in the property list, but it cannot be smaller. 


## -returns



On success, the <b>CWiauPropertyList::Init</b> method returns S_OK. If the method has already been called on a given property list, the method returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540389">CWiauPropertyList::CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>
 

 

