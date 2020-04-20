---
UID: NF:wmp.IWMPControls.fastForward
title: IWMPControls::fastForward (wmp.h)
description: The fastForward method starts fast play of the media item in the forward direction.helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","fastForward method","IWMPControls.fastForward","IWMPControls::fastForward","IWMPControlsfastForward","fastForward","fastForward method [Windows Media Player]","fastForward method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_fastforward","wmp/IWMPControls::fastForward"]
old-location: wmp\iwmpcontrols_fastforward.htm
tech.root: WMP
ms.assetid: a741da8d-f1a2-4a96-acb6-7c40077f6b5e
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],fastForward method, IWMPControls.fastForward, IWMPControls::fastForward, IWMPControlsfastForward, fastForward, fastForward method [Windows Media Player], fastForward method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_fastforward, wmp/IWMPControls::fastForward
f1_keywords:
- wmp/IWMPControls.fastForward
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
- IWMPControls.fastForward
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_isavailable">IWMPControls::get_isAvailable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">IWMPControls::stop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_rate">IWMPSettings::put_rate</a>
 

 

