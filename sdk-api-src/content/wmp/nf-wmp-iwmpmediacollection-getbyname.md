---
UID: NF:wmp.IWMPMediaCollection.getByName
title: IWMPMediaCollection::getByName
author: windows-sdk-content
description: The getByName method retrieves a pointer to an IWMPPlaylist interface. This interface contains the media items with the specified name.
old-location: wmp\iwmpmediacollection_getbyname.htm
old-project: WMP
ms.assetid: 114b0449-a45e-42e5-9e68-428c40a388cf
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByName method, IWMPMediaCollection.getByName, IWMPMediaCollection::getByName, IWMPMediaCollectiongetByName, getByName, getByName method [Windows Media Player], getByName method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyname, wmp/IWMPMediaCollection::getByName
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
-	IWMPMediaCollection.getByName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaCollection::getByName


## -description



The <b>getByName</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface contains the media items with the specified name.




## -parameters




### -param bstrName [in]

String containing the specified name.


### -param ppMediaItems [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the retrieved media items.


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

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByName</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/41b090ca-edf0-440e-b578-26c5ad064657">IWMPCore::get_mediaCollection</a>, then the <b>getByName</b> method returns all the media items in the library that have the specified name. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/6de39a4e-fcce-401b-9bbf-7b06d1fb0370">IWMPLibrary::get_mediaCollection</a>, then the <b>getByName</b> method returns only the audio items in the library that have the specified name.




## -see-also




<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>
 

 

