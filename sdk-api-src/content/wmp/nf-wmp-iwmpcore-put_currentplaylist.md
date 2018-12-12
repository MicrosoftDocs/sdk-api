---
UID: NF:wmp.IWMPCore.put_currentPlaylist
title: IWMPCore::put_currentPlaylist
author: windows-sdk-content
description: The put_currentPlaylist method specifies the IWMPPlaylist interface that corresponds to the current playlist.
old-location: wmp\iwmpcore_put_currentplaylist.htm
tech.root: WMP
ms.assetid: 943641ca-9733-4066-bc69-834e792d93dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCore interface [Windows Media Player],put_currentPlaylist method, IWMPCore.put_currentPlaylist, IWMPCore::put_currentPlaylist, IWMPCoreput_currentPlaylist, put_currentPlaylist, put_currentPlaylist method [Windows Media Player], put_currentPlaylist method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_put_currentplaylist, wmp/IWMPCore::put_currentPlaylist
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
 - IWMPCore.put_currentPlaylist
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::put_currentPlaylist


## -description



The <b>put_currentPlaylist</b> method specifies the <b>IWMPPlaylist</b> interface that corresponds to the current playlist.




## -parameters




### -param pPL [in]

Pointer to an <b>IWMPPlaylist</b> interface.


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



If the <b>IWMPSettings::put_autoStart</b> method was invoked with an argument of true, file playback will begin automatically whenever you invoke <b>put_currentPlaylist</b>.

You can retrieve an <b>IWMPMedia</b> interface for a given media object by invoking the <b>IWMPPlaylist::get_Item</b> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563228(v=VS.85).aspx">IWMPCore::get_currentPlaylist</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>
 

 

