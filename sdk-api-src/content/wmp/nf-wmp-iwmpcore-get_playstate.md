---
UID: NF:wmp.IWMPCore.get_playState
title: IWMPCore::get_playState (wmp.h)
author: windows-sdk-content
description: The get_playState method retrieves an enumeration value indicating the operating state of Windows Media Player.
old-location: wmp\iwmpcore_get_playstate.htm
tech.root: WMP
ms.assetid: cadac1c6-fff6-44aa-a6ce-2b2f69da2d78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_playState method, IWMPCore.get_playState, IWMPCore::get_playState, IWMPCoreget_playState, get_playState, get_playState method [Windows Media Player], get_playState method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_playstate, wmp/IWMPCore::get_playState
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
 - IWMPCore.get_playState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::get_playState


## -description



The <b>get_playState</b> method retrieves an enumeration value indicating the operating state of Windows Media Player.




## -parameters




### -param pwmpps [out]

Pointer to a <b>WMPPlayState</b> enumeration.


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



Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564881(v=VS.85).aspx">WMPPlayState</a>
 

 

