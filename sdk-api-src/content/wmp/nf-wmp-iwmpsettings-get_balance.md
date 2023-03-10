---
UID: NF:wmp.IWMPSettings.get_balance
title: IWMPSettings::get_balance (wmp.h)
description: The get_balance method retrieves the current stereo balance.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_balance method","IWMPSettings.get_balance","IWMPSettings::get_balance","IWMPSettingsget_balance","get_balance","get_balance method [Windows Media Player]","get_balance method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_balance","wmp/IWMPSettings::get_balance"]
old-location: wmp\iwmpsettings_get_balance.htm
tech.root: WMP
ms.assetid: 457ee1a8-44da-424d-9cc5-0f0421791757
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_balance method, IWMPSettings.get_balance, IWMPSettings::get_balance, IWMPSettingsget_balance, get_balance, get_balance method [Windows Media Player], get_balance method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_balance, wmp/IWMPSettings::get_balance
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
 - IWMPSettings::get_balance
 - wmp/IWMPSettings::get_balance
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
 - IWMPSettings.get_balance
---

# IWMPSettings::get_balance


## -description

The <b>get_balance</b> method retrieves the current stereo balance.

## -parameters

### -param plBalance [out]

Pointer to a <b>long</b> containing the balance. This value can range from –100 to 100. The default value is zero.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_balance">IWMPSettings::put_balance</a>