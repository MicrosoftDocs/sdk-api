---
UID: NN:wmp.IWMPSyncServices
title: IWMPSyncServices (wmp.h)
author: windows-sdk-content
description: The IWMPSyncServices interface provides methods to enumerate available devices that can synchronize digital media files with Windows Media Player 10 or later.To use this interface, you must create a remoted instance of the Windows Media Player control.
old-location: wmp\iwmpsyncservices.htm
tech.root: WMP
ms.assetid: 57db3646-2f79-4087-98b2-2bc9d2f3c866
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPSyncServices, IWMPSyncServices interface [Windows Media Player], IWMPSyncServices interface [Windows Media Player],described, IWMPSyncServicesInterface, wmp.iwmpsyncservices, wmp/IWMPSyncServices
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPSyncServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncServices interface


## -description



The <b>IWMPSyncServices</b> interface provides methods to enumerate available devices that can synchronize digital media files with Windows Media Player 10 or later.

To use this interface, you must create a remoted instance of the Windows Media Player control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPSyncServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563750(v=VS.85).aspx">get_deviceCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of available devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563749(v=VS.85).aspx">getDevice</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to a device interface.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPSyncServices</b> by calling <b>QueryInterface</b> through <a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer</a>.

	


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

