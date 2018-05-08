---
UID: NF:wmp.IWMPControls.play
title: IWMPControls::play
author: windows-driver-content
description: The play method causes the current media item to start playing, or resumes play of a paused item.
old-location: wmp\iwmpcontrols_play.htm
old-project: WMP
ms.assetid: 45b5634b-6d23-4e61-90e4-ef0cc9d90a14
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPControls interface [Windows Media Player],play method, IWMPControls.play, IWMPControls::play, IWMPControlsplay, play, play method [Windows Media Player], play method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_play, wmp/IWMPControls::play
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
-	IWMPControls.play
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::play


## -description



The <b>play</b> method causes the current media item to start playing, or resumes play of a paused item.




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



If this method is called while fast-forwarding or rewinding, the rate of playback is set to 1.0.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/8d4282b0-08a9-4c66-ab8b-93429e77e05d">IWMPControls::playItem</a>
 

 

