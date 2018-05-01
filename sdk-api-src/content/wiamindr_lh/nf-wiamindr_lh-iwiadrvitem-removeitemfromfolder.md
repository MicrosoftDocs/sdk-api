---
UID: NF:wiamindr_lh.IWiaDrvItem.RemoveItemFromFolder
title: IWiaDrvItem::RemoveItemFromFolder method
author: windows-driver-content
description: The IWiaDrvItem::RemoveItemFromFolder method removes an item from a parent folder.
old-location: image\iwiadrvitem_removeitemfromfolder.htm
old-project: image
ms.assetid: f800427e-d6b6-4f4c-aee7-4b2b0d0aa0c4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: DrvItem_240e14a4-36bd-4a72-b143-6f8f5c220682.xml, IWiaDrvItem, IWiaDrvItem interface [Imaging Devices], RemoveItemFromFolder method, IWiaDrvItem::RemoveItemFromFolder, RemoveItemFromFolder method [Imaging Devices], RemoveItemFromFolder method [Imaging Devices], IWiaDrvItem interface, RemoveItemFromFolder,IWiaDrvItem.RemoveItemFromFolder, image.iwiadrvitem_removeitemfromfolder, wiamindr_lh/IWiaDrvItem::RemoveItemFromFolder
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
-	IWiaDrvItem.RemoveItemFromFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDrvItem::RemoveItemFromFolder method


## -description


The <b>IWiaDrvItem::RemoveItemFromFolder</b> method removes an item from a parent folder.


## -parameters




### -param __MIDL__IWiaDrvItem0006






#### - lReason [in]

Specifies the reason for the removal of the item from the folder. This parameter can be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WiaItemTypeDeleted 

</td>
<td>
The item is marked as deleted.

</td>
</tr>
<tr>
<td>
WiaItemTypeDisconnected

</td>
<td>
The item is a disconnected device.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If the item to be removed is a folder and the folder is not empty, the method returns E_INVALIDARG. If <i>lReason</i> contains an invalid reason, the method returns E_INVALIDARG. If the method fails for another reason, it returns a standard COM error code.




## -remarks



After the item has been removed from the folder, it can no longer be used for device access.




## -see-also




<a href="https://msdn.microsoft.com/0609e1b2-48df-413c-90bd-d7ddea26510a">IWiaDrvItem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543856">IWiaDrvItem::AddItemToFolder</a>
 

 

