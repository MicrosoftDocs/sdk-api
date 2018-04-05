---
UID: NF:wmp.IWMPCdromRip.get_ripState
title: IWMPCdromRip::get_ripState method
author: windows-driver-content
description: The get_ripState method retrieves an enumeration value that indicates the current state of the ripping process.
old-location: wmp\iwmpcdromrip_get_ripstate.htm
old-project: WMP
ms.assetid: 81c7ba1d-81d7-4f64-9f7d-c88d6959bee0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPCdromRip, IWMPCdromRip interface [Windows Media Player], get_ripState method, IWMPCdromRip::get_ripState, IWMPCdromRipget_ripState, get_ripState method [Windows Media Player], get_ripState method [Windows Media Player], IWMPCdromRip interface, get_ripState,IWMPCdromRip.get_ripState, wmp.iwmpcdromrip_get_ripstate, wmp/IWMPCdromRip::get_ripState
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
-	IWMPCdromRip.get_ripState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromRip::get_ripState method


## -description



The <b>get_ripState</b> method retrieves an enumeration value that indicates the current state of the ripping process.




## -parameters




### -param pwmprs [out]

Pointer to a variable that receives a value from the <b>WMPRipState</b> enumeration that indicates the current state.


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




<a href="https://msdn.microsoft.com/c3e2db46-bef0-4c79-91b5-97ca5a86c6ba">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/f5c1b5bf-d616-48cb-8690-e0237c56e402">Ripping a CD</a>



<a href="https://msdn.microsoft.com/bd62cae1-3f63-4355-afc7-e429a444189d">WMPRipState</a>
 

 

