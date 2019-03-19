---
UID: NF:wmp.IWMPPlaylist.get_count
title: IWMPPlaylist::get_count (wmp.h)
author: windows-sdk-content
description: The get_count method retrieves the number of items in the playlist.
old-location: wmp\iwmpplaylist_get_count.htm
tech.root: WMP
ms.assetid: e37d1d96-27c3-415a-ac85-ab4b94dbc688
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_count method, IWMPPlaylist.get_count, IWMPPlaylist::get_count, IWMPPlaylistget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_count, wmp/IWMPPlaylist::get_count
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
 - IWMPPlaylist.get_count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlaylist::get_count


## -description



The <b>get_count</b> method retrieves the number of items in the playlist.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> containing the count.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>
 

 

