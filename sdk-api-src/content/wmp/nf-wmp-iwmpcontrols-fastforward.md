---
UID: NF:wmp.IWMPControls.fastForward
title: IWMPControls::fastForward
author: windows-sdk-content
description: The fastForward method starts fast play of the media item in the forward direction.
old-location: wmp\iwmpcontrols_fastforward.htm
old-project: WMP
ms.assetid: a741da8d-f1a2-4a96-acb6-7c40077f6b5e
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPControls interface [Windows Media Player],fastForward method, IWMPControls.fastForward, IWMPControls::fastForward, IWMPControlsfastForward, fastForward, fastForward method [Windows Media Player], fastForward method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_fastforward, wmp/IWMPControls::fastForward
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
 - IWMPControls.fastForward
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::fastForward


## -description



The <b>fastForward</b> method starts fast play of the media item in the forward direction.




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



The <b>fastForward</b> method plays the clip back at five times the normal speed. Calling <b>fastForward</b> is equivalent to specifying 5.0 for the rate through the <b>IWMPSettings::put_rate</b> method. If the rate is subsequently changed, or if <b>IWMPControls::play</b> or <b>IWMPControls::stop</b> is called, Windows Media Player will cease fast forwarding.

The <b>fastForward</b> method does not work for live broadcasts and certain media types. To determine whether you can fast forward in a clip, call the <b>IWMPControls::get_isAvailable</b> method and pass in the <b>BSTR</b> value "FastForward".




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/702e09f2-e086-45e3-9ae1-b62ec3e9561f">IWMPControls::get_isAvailable</a>



<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/97ab009d-5ad9-4049-a212-1ef95941f951">IWMPControls::stop</a>



<a href="https://msdn.microsoft.com/a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2">IWMPSettings::put_rate</a>
 

 

