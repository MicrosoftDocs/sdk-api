---
UID: NF:wmp.IWMPControls.next
title: IWMPControls::next
author: windows-sdk-content
description: The next method sets the next item in the playlist as the current item.
old-location: wmp\iwmpcontrols_next.htm
tech.root: WMP
ms.assetid: 1f0bbc77-b271-4076-8089-92fe7745d9a8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPControls interface [Windows Media Player],next method, IWMPControls.next, IWMPControls::next, IWMPControlsnext, next, next method [Windows Media Player], next method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_next, wmp/IWMPControls::next
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
 - IWMPControls.next
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
- IWMPControls.next
: 
---

# IWMPControls::next


## -description



The <b>next</b> method sets the next item in the playlist as the current item.




## -parameters






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



If the playlist is on the last entry when <b>next</b> is invoked, the first entry in the playlist will become the current one.

For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.

When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist. When playing DVD stills, this method skips to the next still.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/e26eca59-1e2d-4a1f-b133-e337a934014b">IWMPControls::previous</a>



<a href="https://msdn.microsoft.com/97ab009d-5ad9-4049-a212-1ef95941f951">IWMPControls::stop</a>
 

 

