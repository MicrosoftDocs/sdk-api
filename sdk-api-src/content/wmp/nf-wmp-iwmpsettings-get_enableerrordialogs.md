---
UID: NF:wmp.IWMPSettings.get_enableErrorDialogs
title: IWMPSettings::get_enableErrorDialogs
author: windows-sdk-content
description: The get_enableErrorDialogs method retrieves a value indicating whether error dialog boxes are displayed automatically.
old-location: wmp\iwmpsettings_get_enableerrordialogs.htm
old-project: WMP
ms.assetid: 557493ea-b685-44e4-b8c3-3f8c5fbe49b8
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_enableErrorDialogs method, IWMPSettings.get_enableErrorDialogs, IWMPSettings::get_enableErrorDialogs, IWMPSettingsget_enableErrorDialogs, get_enableErrorDialogs, get_enableErrorDialogs method [Windows Media Player], get_enableErrorDialogs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_enableerrordialogs, wmp/IWMPSettings::get_enableErrorDialogs
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
-	IWMPSettings.get_enableErrorDialogs
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::get_enableErrorDialogs


## -description



The <b>get_enableErrorDialogs</b> method retrieves a value indicating whether error dialog boxes are displayed automatically.




## -parameters




### -param pfEnableErrorDialogs [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether error dialog boxes are displayed automatically. The default is <b>TRUE</b>.


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



<a href="https://msdn.microsoft.com/c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393">IWMPSettings::put_enableErrorDialogs</a>
 

 

