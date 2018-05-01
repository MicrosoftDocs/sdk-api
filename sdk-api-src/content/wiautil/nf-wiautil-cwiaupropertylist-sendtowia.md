---
UID: NF:wiautil.CWiauPropertyList.SendToWia
title: CWiauPropertyList::SendToWia method
author: windows-driver-content
description: The CWiauPropertyList::SendToWia method calls the WIA service to define all of the properties currently contained in the property list object.
old-location: image\cwiaupropertylist_sendtowia.htm
old-project: image
ms.assetid: 2f7d6975-4c90-4351-bf68-89786bafcc8e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], SendToWia method, CWiauPropertyList::SendToWia, SendToWia method [Imaging Devices], SendToWia method [Imaging Devices], CWiauPropertyList interface, SendToWia,CWiauPropertyList.SendToWia, image.cwiaupropertylist_sendtowia, wiauFncs_d77b66a2-1c98-4608-9269-ab1e09a98405.xml, wiautil/CWiauPropertyList::SendToWia
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
-	CWiauPropertyList.SendToWia
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::SendToWia method


## -description


The <b>CWiauPropertyList::SendToWia</b> method calls the WIA service to define all of the properties currently contained in the property list object. 


## -parameters




### -param pWiasContext

Pointer to a WIA item context that previously was passed in a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544989">IWiaMiniDrv::drvInitItemProperties</a> method.


## -returns



On success, the <b>CWiauPropertyList::SendToWia</b> method returns S_OK. If the property list contains no properties, the method returns E_FAIL. 




## -remarks



The <b>CWiauPropertyList::SendToWia</b> method should be called only after all properties have been defined and their values set.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544989">IWiaMiniDrv::drvInitItemProperties</a>
 

 

