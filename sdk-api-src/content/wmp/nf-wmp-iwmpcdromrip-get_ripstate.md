---
UID: NF:wmp.IWMPCdromRip.get_ripState
title: IWMPCdromRip::get_ripState (wmp.h)
author: windows-sdk-content
description: The get_ripState method retrieves an enumeration value that indicates the current state of the ripping process.
old-location: wmp\iwmpcdromrip_get_ripstate.htm
tech.root: WMP
ms.assetid: 81c7ba1d-81d7-4f64-9f7d-c88d6959bee0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCdromRip interface [Windows Media Player],get_ripState method, IWMPCdromRip.get_ripState, IWMPCdromRip::get_ripState, IWMPCdromRipget_ripState, get_ripState, get_ripState method [Windows Media Player], get_ripState method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_get_ripstate, wmp/IWMPCdromRip::get_ripState
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
 - IWMPCdromRip.get_ripState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCdromRip::get_ripState


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563102(v=VS.85).aspx">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/f5c1b5bf-d616-48cb-8690-e0237c56e402">Ripping a CD</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564884(v=VS.85).aspx">WMPRipState</a>
 

 

