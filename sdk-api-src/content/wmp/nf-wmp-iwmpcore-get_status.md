---
UID: NF:wmp.IWMPCore.get_status
title: IWMPCore::get_status
author: windows-sdk-content
description: The get_status method retrieves the status of Windows Media Player.
old-location: wmp\iwmpcore_get_status.htm
tech.root: WMP
ms.assetid: ee11cb36-4dd2-4fe4-84fd-b3fc11b13ae0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_status method, IWMPCore.get_status, IWMPCore::get_status, IWMPCoreget_status, get_status, get_status method [Windows Media Player], get_status method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_status, wmp/IWMPCore::get_status
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
 - IWMPCore.get_status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::get_status


## -description



The <b>get_status</b> method retrieves the status of Windows Media Player.




## -parameters




### -param pbstrStatus [out]

Pointer to a <b>BSTR</b> containing the status.


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



The values returned by this method are subject to change at any time, and should be used for display purposes only.

The <b>IWMPEvents::StatusChange</b> event is fired whenever this property changes value.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/0397ae20-bc8b-4b7e-8d5d-2b1fb427355a">IWMPEvents::StatusChange</a>
 

 

