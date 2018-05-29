---
UID: NF:wmp.IWMPCore.get_currentMedia
title: IWMPCore::get_currentMedia
author: windows-sdk-content
description: The get_currentMedia method retrieves a pointer to an IWMPMedia interface corresponding to the current media item.
old-location: wmp\iwmpcore_get_currentmedia.htm
old-project: WMP
ms.assetid: 4f199336-0555-40de-8d27-780b05ef9510
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_currentMedia method, IWMPCore.get_currentMedia, IWMPCore::get_currentMedia, IWMPCoreget_currentMedia, get_currentMedia, get_currentMedia method [Windows Media Player], get_currentMedia method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_currentmedia, wmp/IWMPCore::get_currentMedia
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCore.get_currentMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::get_currentMedia


## -description



The <b>get_currentMedia</b> method retrieves a pointer to an <b>IWMPMedia</b> interface corresponding to the current media item.




## -parameters




### -param ppMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface.


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




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">IWMPMedia::put_currentMedia</a>
 

 

