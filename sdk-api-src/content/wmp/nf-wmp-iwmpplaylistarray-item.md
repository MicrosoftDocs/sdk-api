---
UID: NF:wmp.IWMPPlaylistArray.item
title: IWMPPlaylistArray::item
author: windows-sdk-content
description: The item method retrieves a pointer to an IWMPPlaylist interface representing the playlist at the specified index.
old-location: wmp\iwmpplaylistarray_item.htm
old-project: WMP
ms.assetid: 2ba85800-12b9-4f14-8d68-ff6a01167308
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPPlaylistArray interface [Windows Media Player],item method, IWMPPlaylistArray.item, IWMPPlaylistArray::item, IWMPPlaylistArrayitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPPlaylistArray interface, wmp.iwmpplaylistarray_item, wmp/IWMPPlaylistArray::item
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
 - IWMPPlaylistArray.item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistArray::item


## -description



The <b>item</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface representing the playlist at the specified index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index that identifies the playlist that the method should retrieve.


### -param ppItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the retrieved playlist.


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




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/e6fb0ed1-cdc1-4792-98cb-2acf27bce5ce">IWMPPlaylistArray Interface</a>
 

 

