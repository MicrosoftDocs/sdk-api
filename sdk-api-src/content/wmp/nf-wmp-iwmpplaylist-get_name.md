---
UID: NF:wmp.IWMPPlaylist.get_name
title: IWMPPlaylist::get_name
author: windows-sdk-content
description: The get_name method retrieves the name of the playlist.
old-location: wmp\iwmpplaylist_get_name.htm
old-project: WMP
ms.assetid: 547a8ebe-b7c7-4dbc-96c4-1d5f5ef77f97
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_name method, IWMPPlaylist.get_name, IWMPPlaylist::get_name, IWMPPlaylistget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_name, wmp/IWMPPlaylist::get_name
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
 - IWMPPlaylist.get_name
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylist::get_name


## -description



The <b>get_name</b> method retrieves the name of the playlist.




## -parameters




### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name.


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




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/749dae2f-d9c3-4bbb-9a2f-042388f5ce0c">IWMPPlaylist::put_name</a>
 

 

