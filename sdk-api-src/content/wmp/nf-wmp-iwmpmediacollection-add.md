---
UID: NF:wmp.IWMPMediaCollection.add
title: IWMPMediaCollection::add
author: windows-sdk-content
description: The add method adds a new media item or playlist to the library.
old-location: wmp\iwmpmediacollection_add.htm
old-project: WMP
ms.assetid: f9dfefbc-c240-41c0-abb9-4bc5012c147c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],add method, IWMPMediaCollection.add, IWMPMediaCollection::add, IWMPMediaCollectionadd, add, add method [Windows Media Player], add method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_add, wmp/IWMPMediaCollection::add
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
-	IWMPMediaCollection.add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaCollection::add


## -description



The <b>add</b> method adds a new media item or playlist to the library.




## -parameters




### -param bstrURL [in]

String containing the URL that specifies the location of the media item or playlist.


### -param ppItem [out]

Pointer to a pointer to the <b>IWMPMedia</b> interface for the added item or playlist.


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



This method loads an existing media item or playlist into the library, given a path. This method does not move or change the file. This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.

This method accepts both static and auto playlist files. The <b>IWMPPlaylistCollection::importPlaylist</b> method can also be used to add a static playlist to the library.

Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/646d2e3c-623b-4040-af82-1cefac6fc1ae">IWMPMediaCollection::remove</a>



<a href="https://msdn.microsoft.com/421a1bd3-65c1-4d8f-be75-918b1cfa06d2">IWMPPlaylistCollection::importPlaylist</a>
 

 

