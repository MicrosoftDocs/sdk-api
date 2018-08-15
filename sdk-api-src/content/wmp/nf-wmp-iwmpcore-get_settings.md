---
UID: NF:wmp.IWMPCore.get_settings
title: IWMPCore::get_settings
author: windows-sdk-content
description: The get_settings method retrieves a pointer to an IWMPSettings interface.
old-location: wmp\iwmpcore_get_settings.htm
old-project: WMP
ms.assetid: 4bbffaff-99e4-4aae-9b8f-cdb86648fdd9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_settings method, IWMPCore.get_settings, IWMPCore::get_settings, IWMPCoreget_settings, get_settings, get_settings method [Windows Media Player], get_settings method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_settings, wmp/IWMPCore::get_settings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCore.get_settings
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>
 

 

