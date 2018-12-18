---
UID: NF:wmp.IWMPSettings.put_enableErrorDialogs
title: IWMPSettings::put_enableErrorDialogs
author: windows-sdk-content
description: The put_enableErrorDialogs method specifies a value indicating whether error dialog boxes are displayed automatically.
old-location: wmp\iwmpsettings_put_enableerrordialogs.htm
tech.root: WMP
ms.assetid: c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_enableErrorDialogs method, IWMPSettings.put_enableErrorDialogs, IWMPSettings::put_enableErrorDialogs, IWMPSettingsput_enableErrorDialogs, put_enableErrorDialogs, put_enableErrorDialogs method [Windows Media Player], put_enableErrorDialogs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_enableerrordialogs, wmp/IWMPSettings::put_enableErrorDialogs
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
 - IWMPSettings.put_enableErrorDialogs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd563648(v=VS.85).aspx">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563660(v=VS.85).aspx">IWMPSettings::get_enableErrorDialogs</a>
 

 

