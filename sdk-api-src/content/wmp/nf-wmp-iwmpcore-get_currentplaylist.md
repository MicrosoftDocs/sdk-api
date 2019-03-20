---
UID: NF:wmp.IWMPCore.get_currentPlaylist
title: IWMPCore::get_currentPlaylist (wmp.h)
author: windows-sdk-content
description: The get_currentPlaylist method retrieves a pointer to an IWMPPlaylist interface corresponding to the current playlist.
old-location: wmp\iwmpcore_get_currentplaylist.htm
tech.root: WMP
ms.assetid: bb923325-67d2-4d73-b7ec-49e9b52cabba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_currentPlaylist method, IWMPCore.get_currentPlaylist, IWMPCore::get_currentPlaylist, IWMPCoreget_currentPlaylist, IWMPPlayer4.get_currentPlaylist, get_currentPlaylist, get_currentPlaylist method [Windows Media Player], get_currentPlaylist method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_currentplaylist, wmp/IWMPCore::get_currentPlaylist
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
 - IWMPCore.get_currentPlaylist
 - IWMPPlayer4.get_currentPlaylist
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::get_currentPlaylist


## -description



The <b>get_currentPlaylist</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface corresponding to the current playlist.




## -parameters




### -param ppPL [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface.


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563242(v=VS.85).aspx">IWMPCore::put_currentPlaylist</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>
 

 

