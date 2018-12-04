---
UID: NF:wmp.IWMPPlayerApplication.get_playerDocked
title: IWMPPlayerApplication::get_playerDocked
author: windows-sdk-content
description: The get_playerDocked method retrieves a value indicating whether Windows Media Player is in a docked state.
old-location: wmp\iwmpplayerapplication_get_playerdocked.htm
tech.root: WMP
ms.assetid: ca590b80-433d-4a9f-9d6b-cbb33d328fda
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],get_playerDocked method, IWMPPlayerApplication.get_playerDocked, IWMPPlayerApplication::get_playerDocked, IWMPPlayerApplicationget_playerDocked, get_playerDocked, get_playerDocked method [Windows Media Player], get_playerDocked method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_get_playerdocked, wmp/IWMPPlayerApplication::get_playerDocked
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
 - IWMPPlayerApplication.get_playerDocked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayerApplication::get_playerDocked


## -description



The <b>get_playerDocked</b> method retrieves a value indicating whether Windows Media Player is in a docked state.




## -parameters




### -param pbPlayerDocked [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether Windows Media Player is in a docked state.


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



This method is used only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bcdd7ea9-66b2-40e9-89a1-0fec073ccd92">IWMPPlayerApplication Interface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

