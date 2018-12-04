---
UID: NF:wmp.IWMPSettings.put_balance
title: IWMPSettings::put_balance
author: windows-sdk-content
description: The put_balance method specifies the current stereo balance.
old-location: wmp\iwmpsettings_put_balance.htm
tech.root: WMP
ms.assetid: bb198bc0-a0cf-4f6b-9a1e-f9a552db7092
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_balance method, IWMPSettings.put_balance, IWMPSettings::put_balance, IWMPSettingsput_balance, put_balance, put_balance method [Windows Media Player], put_balance method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_balance, wmp/IWMPSettings::put_balance
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
 - IWMPSettings.put_balance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/457ee1a8-44da-424d-9cc5-0f0421791757">IWMPSettings::get_balance</a>
 

 

