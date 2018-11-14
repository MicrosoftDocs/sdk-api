---
UID: NF:wmp.IWMPPlaylist.insertItem
title: IWMPPlaylist::insertItem
author: windows-sdk-content
description: The insertItem method adds a media item at the specified location in the playlist.
old-location: wmp\iwmpplaylist_insertitem.htm
tech.root: WMP
ms.assetid: 2db2d28d-4cbf-423c-824f-e1e212c46f7a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],insertItem method, IWMPPlaylist.insertItem, IWMPPlaylist::insertItem, IWMPPlaylistinsertItem, insertItem, insertItem method [Windows Media Player], insertItem method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_insertitem, wmp/IWMPPlaylist::insertItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlaylist.insertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPPlaylist.insertItem
: 
---

# IWMPPlaylist::insertItem


## -description



The <b>insertItem</b> method adds a media item at the specified location in the playlist.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index at which this method will add the item.


### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface for the inserted item.


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



All items after the inserted item will have their index numbers increased by one.

Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/7a17b0e0-2eaf-4570-a297-c2540ae4b6c5">IWMPPlaylist::removeItem</a>
 

 

