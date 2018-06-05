---
UID: NF:wmp.IWMPPlayer4.get_isRemote
title: IWMPPlayer4::get_isRemote
author: windows-sdk-content
description: The get_isRemote method retrieves a value indicating whether the Windows Media Player control is running in remote mode.
old-location: wmp\iwmpplayer4_get_isremote.htm
old-project: WMP
ms.assetid: 0b4f76f2-f62a-4c91-bbc4-166c450608dd
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPPlayer4 interface [Windows Media Player],get_isRemote method, IWMPPlayer4.get_isRemote, IWMPPlayer4::get_isRemote, IWMPPlayer4get_isRemote, get_isRemote, get_isRemote method [Windows Media Player], get_isRemote method [Windows Media Player],IWMPPlayer4 interface, wmp.iwmpplayer4_get_isremote, wmp/IWMPPlayer4::get_isRemote
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPPlayer4.get_isRemote
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayer4::get_isRemote


## -description



The <b>get_isRemote</b> method retrieves a value indicating whether the Windows Media Player control is running in remote mode.




## -parameters




### -param pvarfIsRemote [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the Windows Media Player control is running in remote mode. If the value is <b>TRUE</b>, then the control is running in remote mode. A value of <b>FALSE</b> means the control is running in local mode.


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



<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

