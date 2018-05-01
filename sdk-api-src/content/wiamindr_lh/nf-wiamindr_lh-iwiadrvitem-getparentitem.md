---
UID: NF:wiamindr_lh.IWiaDrvItem.GetParentItem
title: IWiaDrvItem::GetParentItem method
author: windows-driver-content
description: The IWiaDrvItem::GetParentItem gets the parent item of the current item.
old-location: image\iwiadrvitem_getparentitem.htm
old-project: image
ms.assetid: e6197993-b998-424e-ab5d-a91a57c7398c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_47782466-b345-43e7-9fd1-8c4b355c6d46.xml, GetParentItem method [Imaging Devices], GetParentItem method [Imaging Devices], IWiaDrvItem interface, GetParentItem,IWiaDrvItem.GetParentItem, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], GetParentItem method, IWiaDrvItem::GetParentItem, image.iwiadrvitem_getparentitem, wiamindr_lh/IWiaDrvItem::GetParentItem
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
-	IWiaDrvItem.GetParentItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::GetParentItem method


## -description


The <b>IWiaDrvItem::GetParentItem</b> gets the parent item of the current item.


## -parameters




### -param __MIDL__IWiaDrvItem0012






#### - ppIParentItem [out, optional]

Returns a pointer to the parent item of the current item.


## -returns



If the method succeeds, it stores a pointer to the parent item in <i>pplParentItem</i> and returns S_OK. If the parent item is the root item, the method returns S_FALSE. If the method fails, it returns a standard COM error code.




## -remarks



Minidrivers typically use this method to obtain a pointer to the nonroot parent item of the current item.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543878">IWiaDrvItem::GetFirstChildItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543889">IWiaDrvItem::GetNextSiblingItem</a>
 

 

