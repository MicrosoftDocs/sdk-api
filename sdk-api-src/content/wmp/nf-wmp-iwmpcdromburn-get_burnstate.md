---
UID: NF:wmp.IWMPCdromBurn.get_burnState
title: IWMPCdromBurn::get_burnState method
author: windows-driver-content
description: The get_burnState method retrieves an enumeration value that indicates the current burn state.
old-location: wmp\iwmpcdromburn_get_burnstate.htm
old-project: WMP
ms.assetid: a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPCdromBurn, IWMPCdromBurn interface [Windows Media Player], get_burnState method, IWMPCdromBurn::get_burnState, IWMPCdromBurnget_burnState, get_burnState method [Windows Media Player], get_burnState method [Windows Media Player], IWMPCdromBurn interface, get_burnState,IWMPCdromBurn.get_burnState, wmp.iwmpcdromburn_get_burnstate, wmp/IWMPCdromBurn::get_burnState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
-	IWMPCdromBurn.get_burnState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::get_burnState method


## -description



The <b>get_burnState</b> method retrieves an enumeration value that indicates the current burn state.




## -parameters




### -param pwmpbs [out]

Pointer to a variable that receives a value from the <b>WMPBurnState</b> enumeration that indicates the current state.


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



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/fd286f68-4d36-48ae-800e-ad2be4c613c1">WMPBurnState</a>
 

 

