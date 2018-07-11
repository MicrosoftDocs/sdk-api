---
UID: NF:wmp.IWMPCdromBurn.get_burnPlaylist
title: IWMPCdromBurn::get_burnPlaylist
author: windows-sdk-content
description: The get_burnPlaylist method retrieves the current playlist to burn to the CD.
old-location: wmp\iwmpcdromburn_get_burnplaylist.htm
old-project: WMP
ms.assetid: b31f4e87-2029-4001-94c7-268b14807cf0
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnPlaylist method, IWMPCdromBurn.get_burnPlaylist, IWMPCdromBurn::get_burnPlaylist, IWMPCdromBurnget_burnPlaylist, get_burnPlaylist, get_burnPlaylist method [Windows Media Player], get_burnPlaylist method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnplaylist, wmp/IWMPCdromBurn::get_burnPlaylist
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMPCdromBurn.get_burnPlaylist
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::get_burnPlaylist


## -description



The <b>get_burnPlaylist</b> method retrieves the current playlist to burn to the CD.




## -parameters




### -param ppPlaylist [out]

Address of a variable that receives the <b>IWMPPlaylist</b> pointer of the playlist to burn.


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




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/26fad65c-d371-4e7c-a86e-1ddb24175909">IWMPCdromBurn::put_burnPlaylist</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>
 

 

