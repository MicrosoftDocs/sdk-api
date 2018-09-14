---
UID: NF:wmp.IWMPSettings.get_balance
title: IWMPSettings::get_balance
author: windows-sdk-content
description: The get_balance method retrieves the current stereo balance.
old-location: wmp\iwmpsettings_get_balance.htm
tech.root: WMP
ms.assetid: 457ee1a8-44da-424d-9cc5-0f0421791757
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_balance method, IWMPSettings.get_balance, IWMPSettings::get_balance, IWMPSettingsget_balance, get_balance, get_balance method [Windows Media Player], get_balance method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_balance, wmp/IWMPSettings::get_balance
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
 - IWMPSettings.get_balance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/bb198bc0-a0cf-4f6b-9a1e-f9a552db7092">IWMPSettings::put_balance</a>
 

 

