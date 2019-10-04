---
UID: NF:wmp.IWMPCore.get_settings
title: IWMPCore::get_settings (wmp.h)
author: windows-sdk-content
description: The get_settings method retrieves a pointer to an IWMPSettings interface.
old-location: wmp\iwmpcore_get_settings.htm
tech.root: WMP
ms.assetid: 4bbffaff-99e4-4aae-9b8f-cdb86648fdd9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_settings method, IWMPCore.get_settings, IWMPCore::get_settings, IWMPCoreget_settings, get_settings, get_settings method [Windows Media Player], get_settings method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_settings, wmp/IWMPCore::get_settings
ms.topic: method
f1_keywords: 
 - "wmp/IWMPCore.get_settings"
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
 - IWMPCore.get_settings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCore::get_settings


## -description



The <b>get_settings</b> method retrieves a pointer to an <b>IWMPSettings</b> interface.




## -parameters




### -param ppSettings [out]

Pointer to a pointer to an <b>IWMPSettings</b> interface.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>
 

 

