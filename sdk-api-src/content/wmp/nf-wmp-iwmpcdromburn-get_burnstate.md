---
UID: NF:wmp.IWMPCdromBurn.get_burnState
title: IWMPCdromBurn::get_burnState (wmp.h)
description: The get_burnState method retrieves an enumeration value that indicates the current burn state.helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","get_burnState method","IWMPCdromBurn.get_burnState","IWMPCdromBurn::get_burnState","IWMPCdromBurnget_burnState","get_burnState","get_burnState method [Windows Media Player]","get_burnState method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_get_burnstate","wmp/IWMPCdromBurn::get_burnState"]
old-location: wmp\iwmpcdromburn_get_burnstate.htm
tech.root: WMP
ms.assetid: a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnState method, IWMPCdromBurn.get_burnState, IWMPCdromBurn::get_burnState, IWMPCdromBurnget_burnState, get_burnState, get_burnState method [Windows Media Player], get_burnState method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnstate, wmp/IWMPCdromBurn::get_burnState
f1_keywords:
- wmp/IWMPCdromBurn.get_burnState
dev_langs:
- c++
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
- IWMPCdromBurn.get_burnState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdromBurn::get_burnState


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpburnstate">WMPBurnState</a>
 

 

