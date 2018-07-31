---
UID: NF:wmp.IWMPCore.get_controls
title: IWMPCore::get_controls
author: windows-sdk-content
description: The get_controls method retrieves a pointer to an IWMPControls interface.
old-location: wmp\iwmpcore_get_controls.htm
old-project: WMP
ms.assetid: 54d013f1-d71b-4b6a-90b4-0226022a2a0f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_controls method, IWMPCore.get_controls, IWMPCore::get_controls, IWMPCoreget_controls, get_controls, get_controls method [Windows Media Player], get_controls method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_controls, wmp/IWMPCore::get_controls
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCore.get_controls
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::get_controls


## -description



The <b>get_controls</b> method retrieves a pointer to an <b>IWMPControls</b> interface.




## -parameters




### -param ppControl [out]

Pointer to a pointer to an <b>IWMPControls</b> interface.


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
 




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>
 

 

