---
UID: NN:wmp.IWMPSyncDevice2
title: IWMPSyncDevice2
author: windows-sdk-content
description: The IWMPSyncDevice2 interface provides a method that supplements the IWMPSyncDevice interface.To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\iwmpsyncdevice2.htm
old-project: WMP
ms.assetid: b47fc5ea-741d-4e47-baad-afeb659f1079
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSyncDevice2, IWMPSyncDevice2 interface [Windows Media Player], IWMPSyncDevice2 interface [Windows Media Player],described, IWMPSyncDevice2Interface, wmp.iwmpsyncdevice2, wmp/IWMPSyncDevice2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPSyncDevice2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSyncDevice2 interface


## -description



The <b>IWMPSyncDevice2</b> interface provides a method that supplements the <b>IWMPSyncDevice</b> interface.

To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice2</b> interface inherits from <a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice</a>. <b>IWMPSyncDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/664e3e12-125b-4e11-bab5-44f51650983e">setItemInfo</a>
</td>
<td align="left" width="63%">
Specifies an attribute value for a device.

</td>
</tr>
</table> 


Retrieve a pointer to <b>IWMPSyncDevice2</b> by calling <b>QueryInterface</b> through a pointer to <a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice</a>.
	


## -see-also




<a href="https://msdn.microsoft.com/981648e4-0cb1-4d7a-bd3b-50e1b9a7282c">IWMPSyncDevice</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

