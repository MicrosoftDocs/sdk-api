---
UID: NF:wmp.IWMPCore.get_network
title: IWMPCore::get_network
author: windows-sdk-content
description: The get_network method retrieves a pointer to an IWMPNetwork interface.
old-location: wmp\iwmpcore_get_network.htm
old-project: WMP
ms.assetid: 8100008a-50da-4496-9d5a-77bcca94e903
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_network method, IWMPCore.get_network, IWMPCore::get_network, IWMPCoreget_network, get_network, get_network method [Windows Media Player], get_network method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_network, wmp/IWMPCore::get_network
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
 - IWMPCore.get_network
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::get_network


## -description



The <b>get_network</b> method retrieves a pointer to an <b>IWMPNetwork</b> interface.




## -parameters




### -param ppQNI [out]

Pointer to a pointer to an <b>IWMPNetwork</b> interface.


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



Returns the network information handler




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

