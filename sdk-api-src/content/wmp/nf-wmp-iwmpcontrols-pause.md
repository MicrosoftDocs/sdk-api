---
UID: NF:wmp.IWMPControls.pause
title: IWMPControls::pause (wmp.h)
description: The pause method pauses playback of the media item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","pause method","IWMPControls.pause","IWMPControls::pause","IWMPControlspause","pause","pause method [Windows Media Player]","pause method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_pause","wmp/IWMPControls::pause"]
old-location: wmp\iwmpcontrols_pause.htm
tech.root: WMP
ms.assetid: ef8a3f0e-b424-43ab-bb42-83e9f80f5d19
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],pause method, IWMPControls.pause, IWMPControls::pause, IWMPControlspause, pause, pause method [Windows Media Player], pause method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_pause, wmp/IWMPControls::pause
f1_keywords:
- wmp/IWMPControls.pause
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_isavailable">IWMPControls::get_isAvailable</a>
 

 

