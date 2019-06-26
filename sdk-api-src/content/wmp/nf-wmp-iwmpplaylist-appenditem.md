---
UID: NF:wmp.IWMPPlaylist.appendItem
title: IWMPPlaylist::appendItem (wmp.h)
author: windows-sdk-content
description: The appendItem method adds a media item to the end of the playlist.
old-location: wmp\iwmpplaylist_appenditem.htm
tech.root: WMP
ms.assetid: e6db41d8-a4d5-4cab-9612-0562f3e92c25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],appendItem method, IWMPPlaylist.appendItem, IWMPPlaylist::appendItem, IWMPPlaylistappendItem, appendItem, appendItem method [Windows Media Player], appendItem method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_appenditem, wmp/IWMPPlaylist::appendItem
ms.topic: method
f1_keywords: 
 - "wmp/IWMPPlaylist.appendItem"
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
 - IWMPPlaylist.appendItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlaylist::appendItem


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



Before calling this method, you must have full access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>
 

 

