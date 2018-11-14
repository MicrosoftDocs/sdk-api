---
UID: NF:wmp.IWMPControls.pause
title: IWMPControls::pause
author: windows-sdk-content
description: The pause method pauses playback of the media item.
old-location: wmp\iwmpcontrols_pause.htm
tech.root: WMP
ms.assetid: ef8a3f0e-b424-43ab-bb42-83e9f80f5d19
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPControls interface [Windows Media Player],pause method, IWMPControls.pause, IWMPControls::pause, IWMPControlspause, pause, pause method [Windows Media Player], pause method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_pause, wmp/IWMPControls::pause
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
 - IWMPControls.pause
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
- IWMPControls.pause
: 
---

# IWMPControls::pause


## -description



The <b>pause</b> method pauses playback of the media item.




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



When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.

Certain media types cannot be paused, such as live streams. To determine whether a particular media type can be paused, call the <b>IWMPControls::get_isAvailable</b> method and pass in the <b>BSTR</b> value "pause".




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/702e09f2-e086-45e3-9ae1-b62ec3e9561f">IWMPControls::get_isAvailable</a>
 

 

