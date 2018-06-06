---
UID: NF:wmp.IWMPMediaCollection.remove
title: IWMPMediaCollection::remove
author: windows-sdk-content
description: The remove method removes a specified item from the media collection.
old-location: wmp\iwmpmediacollection_remove.htm
old-project: WMP
ms.assetid: 646d2e3c-623b-4040-af82-1cefac6fc1ae
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],remove method, IWMPMediaCollection.remove, IWMPMediaCollection::remove, IWMPMediaCollectionremove, remove, remove method [Windows Media Player], remove method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_remove, wmp/IWMPMediaCollection::remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMediaCollection.remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaCollection::remove


## -description



The <b>remove</b> method removes a specified item from the media collection.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPMedia</b> interface that identifies the item to remove.


### -param varfDeleteFile [in]

Specifies whether the method should remove the specified item.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method deletes an item from the library. This method does not delete files from the user's computer.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/f9dfefbc-c240-41c0-abb9-4bc5012c147c">IWMPMediaCollection::add</a>
 

 

