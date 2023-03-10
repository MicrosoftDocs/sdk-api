---
UID: NF:wmp.IWMPSettings.put_balance
title: IWMPSettings::put_balance (wmp.h)
description: The put_balance method specifies the current stereo balance.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_balance method","IWMPSettings.put_balance","IWMPSettings::put_balance","IWMPSettingsput_balance","put_balance","put_balance method [Windows Media Player]","put_balance method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_balance","wmp/IWMPSettings::put_balance"]
old-location: wmp\iwmpsettings_put_balance.htm
tech.root: WMP
ms.assetid: bb198bc0-a0cf-4f6b-9a1e-f9a552db7092
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_balance method, IWMPSettings.put_balance, IWMPSettings::put_balance, IWMPSettingsput_balance, put_balance, put_balance method [Windows Media Player], put_balance method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_balance, wmp/IWMPSettings::put_balance
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
 - IWMPSettings::put_balance
 - wmp/IWMPSettings::put_balance
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
 - IWMPSettings.put_balance
---

# IWMPSettings::put_balance


## -description

The <b>put_balance</b> method specifies the current stereo balance.

## -parameters

### -param lBalance [in]

<b>long</b> containing the balance. Values range from –100 to 100. The default value is zero.

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

The value zero indicates that the audio plays at equal volume on both left and right channels. A value of –100 indicates that audio plays only on the left channel. A value of 100 indicates that audio plays only on the right channel.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_balance">IWMPSettings::get_balance</a>