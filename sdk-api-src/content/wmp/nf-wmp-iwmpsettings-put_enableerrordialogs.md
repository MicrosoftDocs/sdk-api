---
UID: NF:wmp.IWMPSettings.put_enableErrorDialogs
title: IWMPSettings::put_enableErrorDialogs
author: windows-driver-content
description: The put_enableErrorDialogs method specifies a value indicating whether error dialog boxes are displayed automatically.
old-location: wmp\iwmpsettings_put_enableerrordialogs.htm
old-project: WMP
ms.assetid: c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_enableErrorDialogs method, IWMPSettings.put_enableErrorDialogs, IWMPSettings::put_enableErrorDialogs, IWMPSettingsput_enableErrorDialogs, put_enableErrorDialogs, put_enableErrorDialogs method [Windows Media Player], put_enableErrorDialogs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_enableerrordialogs, wmp/IWMPSettings::put_enableErrorDialogs
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
-	IWMPSettings.put_enableErrorDialogs
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_enableErrorDialogs


## -description



The <b>put_enableErrorDialogs</b> method specifies a value indicating whether error dialog boxes are displayed automatically.




## -parameters




### -param fEnableErrorDialogs [in]

<b>VARIANT_BOOL</b> indicating whether error dialog boxes are displayed automatically. The default is <b>TRUE</b>.


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



This method exhibits specific behavior for remoted instances of the Windows Media Player control. For more information, see <a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/557493ea-b685-44e4-b8c3-3f8c5fbe49b8">IWMPSettings::get_enableErrorDialogs</a>
 

 

