---
UID: NF:wmp.IWMPCore.get_isOnline
title: IWMPCore::get_isOnline (wmp.h)
description: The get_isOnline method retrieves a value indicating whether the user is connected to a network.helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_isOnline method","IWMPCore.get_isOnline","IWMPCore::get_isOnline","IWMPCoreget_isOnline","get_isOnline","get_isOnline method [Windows Media Player]","get_isOnline method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_isonline","wmp/IWMPCore::get_isOnline"]
old-location: wmp\iwmpcore_get_isonline.htm
tech.root: WMP
ms.assetid: 5507a80f-4bef-4712-af41-49e58d8396aa
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_isOnline method, IWMPCore.get_isOnline, IWMPCore::get_isOnline, IWMPCoreget_isOnline, get_isOnline, get_isOnline method [Windows Media Player], get_isOnline method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_isonline, wmp/IWMPCore::get_isOnline
f1_keywords:
- wmp/IWMPCore.get_isOnline
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
- IWMPCore.get_isOnline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCore::get_isOnline


## -description



The <b>get_isOnline</b> method retrieves a value indicating whether the user is connected to a network.




## -parameters




### -param pfOnline [out]

Pointer to a <b>VARIANT_BOOL</b>, <b>true</b> indicating online.


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



<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>
 

 

