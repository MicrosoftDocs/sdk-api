---
UID: NF:wmp.IWMPControls.get_isAvailable
title: IWMPControls::get_isAvailable (wmp.h)
description: The get_isAvailable method indicates whether a specified type of information is available or a specified action can be performed.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","get_isAvailable method","IWMPControls.get_isAvailable","IWMPControls::get_isAvailable","IWMPControlsget_isAvailable","get_isAvailable","get_isAvailable method [Windows Media Player]","get_isAvailable method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_get_isavailable","wmp/IWMPControls::get_isAvailable"]
old-location: wmp\iwmpcontrols_get_isavailable.htm
tech.root: WMP
ms.assetid: 702e09f2-e086-45e3-9ae1-b62ec3e9561f
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_isAvailable method, IWMPControls.get_isAvailable, IWMPControls::get_isAvailable, IWMPControlsget_isAvailable, get_isAvailable, get_isAvailable method [Windows Media Player], get_isAvailable method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_isavailable, wmp/IWMPControls::get_isAvailable
f1_keywords:
- wmp/IWMPControls.get_isAvailable
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
- IWMPControls.get_isAvailable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls::get_isAvailable


## -description



The <b>get_isAvailable</b> method indicates whether a specified type of information is available or a specified action can be performed.




## -parameters




### -param bstrItem [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>currentItem</td>
<td>Determines whether the user can set the <b>IWMPControls::put_currentItem</b> method.</td>
</tr>
<tr>
<td>currentMarker</td>
<td>Determines whether the user can seek to a specific marker.</td>
</tr>
<tr>
<td>currentPosition</td>
<td>Determines whether the user can seek to a specific position in the file. Some files do not support seeking.</td>
</tr>
<tr>
<td>fastForward</td>
<td>Determines whether the file supports fast forwarding and whether that functionality can be invoked. Many file types (or live streams) do not support fastForward.</td>
</tr>
<tr>
<td>fastReverse</td>
<td>Determines whether the file supports fastReverse and whether that functionality can be invoked. Many file types (or live streams) do not support fastReverse.</td>
</tr>
<tr>
<td>next</td>
<td>Determines whether the user can seek to the next entry in a playlist.</td>
</tr>
<tr>
<td>pause</td>
<td>Determines whether the <b>IWMPControls::pause</b> method is available.</td>
</tr>
<tr>
<td>play</td>
<td>Determines whether the <b>IWMPControls::play</b> method is available.</td>
</tr>
<tr>
<td>previous</td>
<td>Determines whether the user can seek to the previous entry in a playlist.</td>
</tr>
<tr>
<td>step</td>
<td>Determines whether the <b>IWMPControls2::step</b> method is available during playback.</td>
</tr>
<tr>
<td>stop</td>
<td>Determines whether the <b>IWMPControls::stop</b> method is available.</td>
</tr>
</table>
 


### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether a specified type of information is available or a specified action can be performed.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols2-step">IWMPControls2::step</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-pause">IWMPControls::pause</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentitem">IWMPControls::put_currentItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">IWMPControls::stop</a>
 

 

