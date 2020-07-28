---
UID: NF:wmp.IWMPSettings.put_enableErrorDialogs
title: IWMPSettings::put_enableErrorDialogs (wmp.h)
description: The put_enableErrorDialogs method specifies a value indicating whether error dialog boxes are displayed automatically.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_enableErrorDialogs method","IWMPSettings.put_enableErrorDialogs","IWMPSettings::put_enableErrorDialogs","IWMPSettingsput_enableErrorDialogs","put_enableErrorDialogs","put_enableErrorDialogs method [Windows Media Player]","put_enableErrorDialogs method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_enableerrordialogs","wmp/IWMPSettings::put_enableErrorDialogs"]
old-location: wmp\iwmpsettings_put_enableerrordialogs.htm
tech.root: WMP
ms.assetid: c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_enableErrorDialogs method, IWMPSettings.put_enableErrorDialogs, IWMPSettings::put_enableErrorDialogs, IWMPSettingsput_enableErrorDialogs, put_enableErrorDialogs, put_enableErrorDialogs method [Windows Media Player], put_enableErrorDialogs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_enableerrordialogs, wmp/IWMPSettings::put_enableErrorDialogs
f1_keywords:
- wmp/IWMPSettings.put_enableErrorDialogs
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This method exhibits specific behavior for remoted instances of the Windows Media Player control. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_enableerrordialogs">IWMPSettings::get_enableErrorDialogs</a>
 

 

