---
UID: NF:wmp.IWMPSettings.get_mute
title: IWMPSettings::get_mute (wmp.h)
description: The get_mute method retrieves a value indicating whether audio is muted.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_mute method","IWMPSettings.get_mute","IWMPSettings::get_mute","IWMPSettingsget_mute","get_mute","get_mute method [Windows Media Player]","get_mute method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_mute","wmp/IWMPSettings::get_mute"]
old-location: wmp\iwmpsettings_get_mute.htm
tech.root: WMP
ms.assetid: b0bb1c84-d208-4d29-a797-bb18af039f03
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_mute method, IWMPSettings.get_mute, IWMPSettings::get_mute, IWMPSettingsget_mute, get_mute, get_mute method [Windows Media Player], get_mute method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_mute, wmp/IWMPSettings::get_mute
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSettings::get_mute
 - wmp/IWMPSettings::get_mute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.get_mute
---

# IWMPSettings::get_mute


## -description

The <b>get_mute</b> method retrieves a value indicating whether audio is muted.

## -parameters

### -param pfMute [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether audio is muted. The default is <b>FALSE</b>.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_rate">IWMPSettings::get_rate</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_mute">IWMPSettings::put_mute</a>