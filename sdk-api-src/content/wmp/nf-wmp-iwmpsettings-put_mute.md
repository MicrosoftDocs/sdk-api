---
UID: NF:wmp.IWMPSettings.put_mute
title: IWMPSettings::put_mute
author: windows-sdk-content
description: The put_mute method specifies a value indicating whether audio is muted.
old-location: wmp\iwmpsettings_put_mute.htm
old-project: WMP
ms.assetid: 644f9a4d-54e4-4e8a-8c02-29feb57c9256
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_mute method, IWMPSettings.put_mute, IWMPSettings::put_mute, IWMPSettingsput_mute, put_mute, put_mute method [Windows Media Player], put_mute method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_mute, wmp/IWMPSettings::put_mute
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSettings.put_mute
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_mute


## -description



The <b>put_mute</b> method specifies a value indicating whether audio is muted.




## -parameters




### -param fMute [in]

<b>VARIANT_BOOL</b> indicating whether audio is muted. The default is <b>FALSE</b>.


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




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/b0bb1c84-d208-4d29-a797-bb18af039f03">IWMPSettings::get_mute</a>



<a href="https://msdn.microsoft.com/a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2">IWMPSettings::put_rate</a>
 

 

