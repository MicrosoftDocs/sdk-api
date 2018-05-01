---
UID: NF:wiamindr_lh.IWiaDrvItem.GetFullItemName
title: IWiaDrvItem::GetFullItemName method
author: windows-driver-content
description: The IWiaDrvItem::GetFullItemName method gets the item's full name, including path information.
old-location: image\iwiadrvitem_getfullitemname.htm
old-project: image
ms.assetid: 810faf49-faa9-45f2-af94-af576f4c1075
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_1b166476-d17a-4953-9c73-6e3d7c9cd0f9.xml, GetFullItemName method [Imaging Devices], GetFullItemName method [Imaging Devices], IWiaDrvItem interface, GetFullItemName,IWiaDrvItem.GetFullItemName, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], GetFullItemName method, IWiaDrvItem::GetFullItemName, image.iwiadrvitem_getfullitemname, wiamindr_lh/IWiaDrvItem::GetFullItemName
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
-	IWiaDrvItem.GetFullItemName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::GetFullItemName method


## -description


The <b>IWiaDrvItem::GetFullItemName</b> method gets the item's full name, including path information.


## -parameters




### -param __MIDL__IWiaDrvItem0002






#### - pbstrFullItemName [out, optional]

Points to a memory location that will receive the address of a string containing the item's full name. 


## -returns



If the method succeeds, it stores a pointer to the item's full name, including path information, in <i>pbstrFullItemName</i> and returns S_OK. If the method fails to allocate the string due to insufficient memory, it returns E_OUTOFMEMORY. If the parameter <i>pbstrFullItemName</i> is invalid, the method returns E_INVALIDARG. If the method fails for another reason, it returns a standard COM error code.




## -remarks



If there is enough memory available, this method allocates a string containing the current item's full name including path information. The method returns a pointer to the string in <i>pbstrFullItemName</i>. The minidriver must deallocate the memory used by the string by calling the <b>SysFreeString</b> function, which is documented in the Microsoft Windows SDK documentation. 

The name returned in <i>pbstrFullItemName </i>is the name associated with the item when the item was first created by the driver services library function <a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>
 

 

