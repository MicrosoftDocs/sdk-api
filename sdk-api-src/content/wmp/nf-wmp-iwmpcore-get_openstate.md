---
UID: NF:wmp.IWMPCore.get_openState
title: IWMPCore::get_openState method
author: windows-driver-content
description: The get_openState method retrieves an enumeration value indicating the state of the content source.
old-location: wmp\iwmpcore_get_openstate.htm
old-project: WMP
ms.assetid: 66c7e52a-d7b4-4c37-a863-fb42f5415c0a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPCore, IWMPCore interface [Windows Media Player], get_openState method, IWMPCore::get_openState, IWMPCoreget_openState, get_openState method [Windows Media Player], get_openState method [Windows Media Player], IWMPCore interface, get_openState,IWMPCore.get_openState, wmp.iwmpcore_get_openstate, wmp/IWMPCore::get_openState
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCore.get_openState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::get_openState method


## -description



The <b>get_openState</b> method retrieves an enumeration value indicating the state of the content source.




## -parameters




### -param pwmpos [out]

Pointer to a <b>WMPOpenState</b> enumeration.


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



Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/535c8f56-d854-449b-ad50-72e5dd32710a">WMPOpenState</a>
 

 

