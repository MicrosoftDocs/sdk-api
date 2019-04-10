---
UID: NF:wmp.IWMPControls.stop
title: IWMPControls::stop (wmp.h)
author: windows-sdk-content
description: The stop method stops playback of the media item.
old-location: wmp\iwmpcontrols_stop.htm
tech.root: WMP
ms.assetid: 97ab009d-5ad9-4049-a212-1ef95941f951
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],stop method, IWMPControls.stop, IWMPControls::stop, IWMPControlsstop, stop, stop method [Windows Media Player], stop method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_stop, wmp/IWMPControls::stop
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
 - IWMPControls.stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::stop


## -description



The <b>stop</b> method stops playback of the media item.




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



This method causes Windows Media Player to release any system resources it is using, such as the audio device. The current media item, however, is not released.

When Windows Media Player is stopped, the current playback point in the media item is reset to the beginning of the item. Subsequently calling <b>IWMPControls::play</b> will start playback from the beginning of the media item. To halt a play operation without changing the current position, use the <b>IWMPControls::pause</b> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563179(v=VS.85).aspx">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563203(v=VS.85).aspx">IWMPControls::next</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563204(v=VS.85).aspx">IWMPControls::pause</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563205(v=VS.85).aspx">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563207(v=VS.85).aspx">IWMPControls::previous</a>
 

 

