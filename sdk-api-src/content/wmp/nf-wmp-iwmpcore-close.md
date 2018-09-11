---
UID: NF:wmp.IWMPCore.close
title: IWMPCore::close
author: windows-sdk-content
description: The close method releases Windows Media Player resources.
old-location: wmp\iwmpcore_close.htm
tech.root: WMP
ms.assetid: e6e21995-5dbd-4893-a9f2-6ce918d3fbc4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPCore interface [Windows Media Player],close method, IWMPCore.close, IWMPCore::close, IWMPCoreclose, close, close method [Windows Media Player], close method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_close, wmp/IWMPCore::close
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
 - IWMPCore.close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::close


## -description



The <b>close</b> method releases Windows Media Player resources.




## -parameters






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



This method closes the current digital media file, not Windows Media Player.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>
 

 

