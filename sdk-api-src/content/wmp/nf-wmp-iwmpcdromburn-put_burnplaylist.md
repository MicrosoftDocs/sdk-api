---
UID: NF:wmp.IWMPCdromBurn.put_burnPlaylist
title: IWMPCdromBurn::put_burnPlaylist
author: windows-sdk-content
description: The put_burnPlaylist method specifies the playlist to burn to CD.
old-location: wmp\iwmpcdromburn_put_burnplaylist.htm
tech.root: WMP
ms.assetid: 26fad65c-d371-4e7c-a86e-1ddb24175909
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],put_burnPlaylist method, IWMPCdromBurn.put_burnPlaylist, IWMPCdromBurn::put_burnPlaylist, IWMPCdromBurnput_burnPlaylist, put_burnPlaylist, put_burnPlaylist method [Windows Media Player], put_burnPlaylist method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_put_burnplaylist, wmp/IWMPCdromBurn::put_burnPlaylist
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPCdromBurn.put_burnPlaylist
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCdromBurn::put_burnPlaylist


## -description



The <b>put_burnPlaylist</b> method specifies the playlist to burn to CD.




## -parameters




### -param pPlaylist [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist to burn.


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



<a href="https://msdn.microsoft.com/b31f4e87-2029-4001-94c7-268b14807cf0">IWMPCdromBurn::get_burnPlaylist</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>
 

 

