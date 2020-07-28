---
UID: NF:wmp.IWMPSettings.get_volume
title: IWMPSettings::get_volume (wmp.h)
description: The get_volume method retrieves the current playback volume.
helpviewer_keywords: ["IWMPSetting2.get_volume","IWMPSetting2::get_volume","IWMPSettings interface [Windows Media Player]","get_volume method","IWMPSettings.get_volume","IWMPSettings::get_volume","IWMPSettingsget_volume","get_volume","get_volume method [Windows Media Player]","get_volume method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_volume","wmp/IWMPSettings::get_volume"]
old-location: wmp\iwmpsettings_get_volume.htm
tech.root: WMP
ms.assetid: 92c217e4-2ec4-4890-810c-dc552a36d578
ms.date: 12/05/2018
ms.keywords: IWMPSetting2.get_volume, IWMPSetting2::get_volume, IWMPSettings interface [Windows Media Player],get_volume method, IWMPSettings.get_volume, IWMPSettings::get_volume, IWMPSettingsget_volume, get_volume, get_volume method [Windows Media Player], get_volume method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_volume, wmp/IWMPSettings::get_volume
f1_keywords:
- wmp/IWMPSettings.get_volume
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
- IWMPSettings.get_volume
- IWMPSetting2::get_volume
- IWMPSetting2.get_volume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings::get_volume


## -description



The <b>get_volume</b> method retrieves the current playback volume.




## -parameters




### -param plVolume [out]

Pointer to a <b>long</b> containing the volume level ranging from 0 to 100.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_volume">IWMPSetting::put_volume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>
 

 

