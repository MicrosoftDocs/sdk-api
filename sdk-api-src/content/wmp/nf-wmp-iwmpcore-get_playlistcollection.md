---
UID: NF:wmp.IWMPCore.get_playlistCollection
title: IWMPCore::get_playlistCollection
author: windows-sdk-content
description: The get_playlistCollection method retrieves a pointer to an IWMPPlaylistCollection interface.
old-location: wmp\iwmpcore_get_playlistcollection.htm
tech.root: WMP
ms.assetid: 8f6ab34f-e055-4a18-b1b8-e3c7b8f9c76a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_playlistCollection method, IWMPCore.get_playlistCollection, IWMPCore::get_playlistCollection, IWMPCoreget_playlistCollection, get_playlistCollection, get_playlistCollection method [Windows Media Player], get_playlistCollection method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_playlistcollection, wmp/IWMPCore::get_playlistCollection
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
 - IWMPCore.get_playlistCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::get_playlistCollection


## -description



The <b>get_playlistCollection</b> method retrieves a pointer to an <b>IWMPPlaylistCollection</b> interface.




## -parameters




### -param ppPlaylistCollection [out]

Pointer to a pointer to an <b>IWMPPlaylistCollection</b> interface.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>
 

 

