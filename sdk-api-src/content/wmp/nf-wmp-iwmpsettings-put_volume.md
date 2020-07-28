---
UID: NF:wmp.IWMPSettings.put_volume
title: IWMPSettings::put_volume (wmp.h)
description: The put_volume method specifies the current playback volume.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_volume method","IWMPSettings.put_volume","IWMPSettings::put_volume","IWMPSettingsput_volume","put_volume","put_volume method [Windows Media Player]","put_volume method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_volume","wmp/IWMPSettings::put_volume"]
old-location: wmp\iwmpsettings_put_volume.htm
tech.root: WMP
ms.assetid: 435dac36-1ccf-41fd-94c2-1242c6af1bbd
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_volume method, IWMPSettings.put_volume, IWMPSettings::put_volume, IWMPSettingsput_volume, put_volume, put_volume method [Windows Media Player], put_volume method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_volume, wmp/IWMPSettings::put_volume
f1_keywords:
- wmp/IWMPSettings.put_volume
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
- IWMPSettings.put_volume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings::put_volume


## -description



The <b>put_volume</b> method specifies the current playback volume.




## -parameters




### -param lVolume [in]

<b>long</b> containing the volume level ranging from 0 to 100.


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



A value of zero specifies no volume (muted). A value of 100 specifies full volume. If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_volume">IWMPSettings::get_volume</a>
 

 

