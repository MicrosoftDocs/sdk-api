---
UID: NF:wmp.IWMPSettings.put_playCount
title: IWMPSettings::put_playCount method
author: windows-driver-content
description: The put_playCount method specifies the number of times a media item will play.
old-location: wmp\iwmpsettings_put_playcount.htm
old-project: WMP
ms.assetid: b9fdd596-8ca3-497e-8d40-6dd5ddbf0a1e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPSettings, IWMPSettings interface [Windows Media Player], put_playCount method, IWMPSettings::put_playCount, IWMPSettingsput_playCount, put_playCount method [Windows Media Player], put_playCount method [Windows Media Player], IWMPSettings interface, put_playCount,IWMPSettings.put_playCount, wmp.iwmpsettings_put_playcount, wmp/IWMPSettings::put_playCount
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSettings.put_playCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_playCount method


## -description



The <b>put_playCount</b> method specifies the number of times a media item will play.




## -parameters




### -param lCount [in]

<b>long</b> containing the count with a minimum value of 1 and a default value of 1.


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



<b>Windows Media Player 10 Mobile: </b>This method is not implemented and always returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/492eb07a-f757-47ce-8474-1edfeb49e55f">IWMPSettings::get_playCount</a>
 

 

