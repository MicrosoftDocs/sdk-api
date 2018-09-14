---
UID: NF:wmp.IWMPPlaylist.get_item
title: IWMPPlaylist::get_item
author: windows-sdk-content
description: The get_item method retrieves the media item at the specified index.
old-location: wmp\iwmpplaylist_get_item.htm
tech.root: WMP
ms.assetid: 20da6e49-720c-4291-9fb7-def441c7fc66
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_item method, IWMPPlaylist.get_item, IWMPPlaylist::get_item, IWMPPlaylistget_item, get_item, get_item method [Windows Media Player], get_item method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_item, wmp/IWMPPlaylist::get_item
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
 - IWMPPlaylist.get_item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlaylist::get_item


## -description



The <b>get_item</b> method retrieves the media item at the specified index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param ppIWMPMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface for the returned item.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>
 

 

