---
UID: NF:wmp.IWMPPlaylist.appendItem
title: IWMPPlaylist::appendItem method
author: windows-driver-content
description: The appendItem method adds a media item to the end of the playlist.
old-location: wmp\iwmpplaylist_appenditem.htm
old-project: WMP
ms.assetid: e6db41d8-a4d5-4cab-9612-0562f3e92c25
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlaylist, IWMPPlaylist interface [Windows Media Player], appendItem method, IWMPPlaylist::appendItem, IWMPPlaylistappendItem, appendItem method [Windows Media Player], appendItem method [Windows Media Player], IWMPPlaylist interface, appendItem,IWMPPlaylist.appendItem, wmp.iwmpplaylist_appenditem, wmp/IWMPPlaylist::appendItem
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPPlaylist.appendItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylist::appendItem method


## -description



The <b>appendItem</b> method adds a media item to the end of the playlist.




## -parameters




### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface.


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



Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>
 

 

