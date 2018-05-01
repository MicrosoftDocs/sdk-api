---
UID: NF:wiamindr_lh.IWiaDrvItem.FindChildItemByName
title: IWiaDrvItem::FindChildItemByName method
author: windows-driver-content
description: The IWiaDrvItem::FindChildItemByName method searches the driver item tree for a specific child item.
old-location: image\iwiadrvitem_findchilditembyname.htm
old-project: image
ms.assetid: 04f446f2-cd59-4191-be0c-60140ecee3b2
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_afe8c47f-ebf9-484e-94bf-fdcd4713ea2a.xml, FindChildItemByName method [Imaging Devices], FindChildItemByName method [Imaging Devices], IWiaDrvItem interface, FindChildItemByName,IWiaDrvItem.FindChildItemByName, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], FindChildItemByName method, IWiaDrvItem::FindChildItemByName, image.iwiadrvitem_findchilditembyname, wiamindr_lh/IWiaDrvItem::FindChildItemByName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiamindr_lh.h
api_name:
-	IWiaDrvItem.FindChildItemByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::FindChildItemByName method


## -description


The <b>IWiaDrvItem::FindChildItemByName</b> method searches the driver item tree for a specific child item.


## -parameters




### -param __MIDL__IWiaDrvItem0010




### -param __MIDL__IWiaDrvItem0011






#### - bstrChildItemName [in]

Specifies a string containing the name with path information of the child item to find.


#### - ppIChildItem [out, optional]

Points to a memory location that will receive the address of the found <b>IWiaDrvItem</b> child item. 


## -returns



If the method succeeds, it stores a pointer to the found child item in <i>ppIChildItem</i> and returns S_OK. If the method fails to find the child item, it returns S_FALSE. If the method fails for another reason, it returns a standard COM error code.




## -remarks



Minidrivers typically use this method to search a driver item tree for a specific child item when the child item's name is known. The child item's full name is obtained in the  method <a href="https://msdn.microsoft.com/library/windows/hardware/ff543881">IWiaDrvItem::GetFullItemName</a>.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543870">IWiaDrvItem::FindItemByName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543881">IWiaDrvItem::GetFullItemName</a>
 

 

