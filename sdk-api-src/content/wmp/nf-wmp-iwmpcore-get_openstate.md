---
UID: NF:wmp.IWMPCore.get_openState
title: IWMPCore::get_openState (wmp.h)
description: The get_openState method retrieves an enumeration value indicating the state of the content source.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_openState method","IWMPCore.get_openState","IWMPCore::get_openState","IWMPCoreget_openState","get_openState","get_openState method [Windows Media Player]","get_openState method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_openstate","wmp/IWMPCore::get_openState"]
old-location: wmp\iwmpcore_get_openstate.htm
tech.root: WMP
ms.assetid: 66c7e52a-d7b4-4c37-a863-fb42f5415c0a
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_openState method, IWMPCore.get_openState, IWMPCore::get_openState, IWMPCoreget_openState, get_openState, get_openState method [Windows Media Player], get_openState method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_openstate, wmp/IWMPCore::get_openState
f1_keywords:
- wmp/IWMPCore.get_openState
dev_langs:
- c++
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
- IWMPCore.get_openState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCore::get_openState


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpopenstate">WMPOpenState</a>
 

 

