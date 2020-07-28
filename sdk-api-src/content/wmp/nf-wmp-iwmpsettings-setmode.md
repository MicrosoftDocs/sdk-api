---
UID: NF:wmp.IWMPSettings.setMode
title: IWMPSettings::setMode (wmp.h)
description: The setMode method sets the state of playback options.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","setMode method","IWMPSettings.setMode","IWMPSettings::setMode","IWMPSettingssetMode","setMode","setMode method [Windows Media Player]","setMode method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_setmode","wmp/IWMPSettings::setMode"]
old-location: wmp\iwmpsettings_setmode.htm
tech.root: WMP
ms.assetid: 28a404a7-5bb0-41bb-a5b2-cc6138b8176e
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],setMode method, IWMPSettings.setMode, IWMPSettings::setMode, IWMPSettingssetMode, setMode, setMode method [Windows Media Player], setMode method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_setmode, wmp/IWMPSettings::setMode
f1_keywords:
- wmp/IWMPSettings.setMode
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
- IWMPSettings.setMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings::setMode


## -description



The <b>setMode</b> method sets the state of playback options.




## -parameters




### -param bstrMode [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>autoRewind</td>
<td>Tracks are restarted at the beginning after playing to the end. Default state is true.</td>
</tr>
<tr>
<td>loop</td>
<td>The sequence of tracks repeats itself. Default state is false.</td>
</tr>
<tr>
<td>showFrame</td>
<td>The nearest video keyframe is displayed when not playing. Default state is false. Has no effect on audio tracks.</td>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order. Default state is false.</td>
</tr>
</table>
 


### -param varfMode [in]

<b>VARIANT_BOOL</b> specifying whether the specified mode is active.


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



When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame. Use this mode cautiously when playing non-local content.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-getmode">IWMPSettings::getMode</a>
 

 

