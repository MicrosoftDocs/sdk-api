---
UID: NF:wiamindr_lh.IWiaDrvItem.GetFirstChildItem
title: IWiaDrvItem::GetFirstChildItem method
author: windows-driver-content
description: The IWiaDrvItem::GetFirstChildItem method gets the first child item in an IWiaDrvItem folder item.
old-location: image\iwiadrvitem_getfirstchilditem.htm
old-project: image
ms.assetid: 2e580a57-03cb-4ff4-b3c6-0b5ef17b4ccb
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_0ee76640-f07a-4b25-9955-230122a2a662.xml, GetFirstChildItem method [Imaging Devices], GetFirstChildItem method [Imaging Devices], IWiaDrvItem interface, GetFirstChildItem,IWiaDrvItem.GetFirstChildItem, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], GetFirstChildItem method, IWiaDrvItem::GetFirstChildItem, image.iwiadrvitem_getfirstchilditem, wiamindr_lh/IWiaDrvItem::GetFirstChildItem
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
-	IWiaDrvItem.GetFirstChildItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::GetFirstChildItem method


## -description


The <b>IWiaDrvItem::GetFirstChildItem</b> method gets the first child item in an <b>IWiaDrvItem</b> folder item.


## -parameters




### -param __MIDL__IWiaDrvItem0013






#### - ppIChildItem [out, optional]

Points to a memory location that will receive the address of an <b>IWiaDrvItem</b> child item.


## -returns



If the method succeeds, it stores a pointer to the first child item in <i>ppIChildItem</i> and returns S_OK. If a child item cannot be found, the method returns S_FALSE. If the item being searched is not a folder, the method returns E_INVALIDARG. If the method fails for another reason, it returns a standard COM error code.




## -remarks



Minidrivers typically use this method to retrieve the first child item in a driver item folder. The item being searched must be a folder item.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543889">IWiaDrvItem::GetNextSiblingItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543892">IWiaDrvItem::GetParentItem</a>
 

 

