---
UID: NF:wmp.IWMPPlayerApplication.get_hasDisplay
title: IWMPPlayerApplication::get_hasDisplay (wmp.h)
author: windows-sdk-content
description: The get_hasDisplay method retrieves a value indicating whether video can display through the remoted Windows Media Player control.
old-location: wmp\iwmpplayerapplication_get_hasdisplay.htm
tech.root: WMP
ms.assetid: a356929a-51de-49b6-bf7a-b3bd7fa35ea2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],get_hasDisplay method, IWMPPlayerApplication.get_hasDisplay, IWMPPlayerApplication::get_hasDisplay, IWMPPlayerApplicationget_hasDisplay, get_hasDisplay, get_hasDisplay method [Windows Media Player], get_hasDisplay method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_get_hasdisplay, wmp/IWMPPlayerApplication::get_hasDisplay
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
 - IWMPPlayerApplication.get_hasDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayerApplication::get_hasDisplay


## -description



The <b>get_hasDisplay</b> method retrieves a value indicating whether video can display through the remoted Windows Media Player control.




## -parameters




### -param pbHasDisplay [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether video can display through the remoted Windows Media Player control.


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

Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls. Use this method to determine whether the current control is the one through which video can be displayed.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563527(v=VS.85).aspx">IWMPPlayerApplication Interface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

