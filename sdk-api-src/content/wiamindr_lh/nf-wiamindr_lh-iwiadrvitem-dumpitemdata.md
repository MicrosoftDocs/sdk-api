---
UID: NF:wiamindr_lh.IWiaDrvItem.DumpItemData
title: IWiaDrvItem::DumpItemData method
author: windows-driver-content
description: The IWiaDrvItem::DumpItemData method dumps private data associated with an IWiaDrvItem item into an allocated private buffer.
old-location: image\iwiadrvitem_dumpitemdata.htm
old-project: image
ms.assetid: e17da654-60a7-4942-99f9-f55df87a1ca3
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_fae1b45f-719d-4bce-92fd-d43844178800.xml, DumpItemData method [Imaging Devices], DumpItemData method [Imaging Devices], IWiaDrvItem interface, DumpItemData,IWiaDrvItem.DumpItemData, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], DumpItemData method, IWiaDrvItem::DumpItemData, image.iwiadrvitem_dumpitemdata, wiamindr_lh/IWiaDrvItem::DumpItemData
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
-	IWiaDrvItem.DumpItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::DumpItemData method


## -description


The <b>IWiaDrvItem::DumpItemData</b> method dumps private data associated with an <b>IWiaDrvItem</b> item into an allocated private buffer.


## -parameters




### -param __MIDL__IWiaDrvItem0015






#### - bstrDrvItemData [out, optional]

Points to an allocated buffer that will receive the <b>IWiaDrvItem</b> data. 


## -returns



If the method succeeds, it returns S_OK. If the method fails the buffer allocation, it returns E_OUTOFMEMORY. If the method fails for another reason, it returns a standard COM error code.




## -remarks



This method is provided for Microsoft internal debugging only. It will return E_NOTIMPL on the release operating system. 



