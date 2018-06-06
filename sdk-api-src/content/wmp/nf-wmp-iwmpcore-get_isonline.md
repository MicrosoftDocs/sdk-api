---
UID: NF:wmp.IWMPCore.get_isOnline
title: IWMPCore::get_isOnline
author: windows-sdk-content
description: The get_isOnline method retrieves a value indicating whether the user is connected to a network.
old-location: wmp\iwmpcore_get_isonline.htm
old-project: WMP
ms.assetid: 5507a80f-4bef-4712-af41-49e58d8396aa
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_isOnline method, IWMPCore.get_isOnline, IWMPCore::get_isOnline, IWMPCoreget_isOnline, get_isOnline, get_isOnline method [Windows Media Player], get_isOnline method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_isonline, wmp/IWMPCore::get_isOnline
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
 - IWMPCore.get_isOnline
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>
 

 

