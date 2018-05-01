---
UID: NF:wiamindr_lh.IWiaDrvItem.GetItemFlags
title: IWiaDrvItem::GetItemFlags method
author: windows-driver-content
description: The IWiaDrvItem::GetItemFlags method gets the item flags of the current IWiaDrvItem item.
old-location: image\iwiadrvitem_getitemflags.htm
old-project: image
ms.assetid: 47358d69-ef45-4cac-8187-72c354912c4e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_6fcac1f5-c754-4158-a1a0-61efe0d3913c.xml, GetItemFlags method [Imaging Devices], GetItemFlags method [Imaging Devices], IWiaDrvItem interface, GetItemFlags,IWiaDrvItem.GetItemFlags, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], GetItemFlags method, IWiaDrvItem::GetItemFlags, image.iwiadrvitem_getitemflags, wiamindr_lh/IWiaDrvItem::GetItemFlags
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
-	IWiaDrvItem.GetItemFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::GetItemFlags method


## -description


The <b>IWiaDrvItem::GetItemFlags</b> method gets the item flags of the current <b>IWiaDrvItem</b> item.


## -parameters




### -param __MIDL__IWiaDrvItem0000






#### - plFlags [out]

Points to a memory location that will receive the item flags.


## -returns



If the method succeeds, it places the item flag values in the location pointed to by <i>plFlags</i> and returns S_OK. If the pointer <i>plFlags</i> is invalid, the method returns E_INVALIDARG. If the method fails for another reason, it returns a standard COM error code.




## -remarks



The method places the current <b>IWiaDrvItem</b> item's flag values in the location pointed to by <i>pIFlags</i>. The item's flag values were set when the item was created by the driver services library function <a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>
 

 

