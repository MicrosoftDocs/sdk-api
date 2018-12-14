---
UID: NF:wmp.IWMPMediaCollection.getByAttribute
title: IWMPMediaCollection::getByAttribute
author: windows-sdk-content
description: The getByAttribute method retrieves a pointer to an IWMPPlaylist interface. This interface corresponds to the specified attribute having the specified value.
old-location: wmp\iwmpmediacollection_getbyattribute.htm
tech.root: WMP
ms.assetid: ab1c53dd-6145-4b2b-a665-4c8c79143284
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByAttribute method, IWMPMediaCollection.getByAttribute, IWMPMediaCollection::getByAttribute, IWMPMediaCollectiongetByAttribute, getByAttribute, getByAttribute method [Windows Media Player], getByAttribute method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyattribute, wmp/IWMPMediaCollection::getByAttribute
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
 - IWMPMediaCollection.getByAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection::getByAttribute


## -description



The <b>getByAttribute</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface corresponds to the specified attribute having the specified value.




## -parameters




### -param bstrAttribute [in]

String containing the specified attribute.


### -param bstrValue [in]

String containing the specified value.


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



This method can be used to create a generic query for media items that match a value for an attribute in the database. This is useful in the case of user-defined attributes. If the attribute does not exist, an error will result.

You can use this method to retrieve all of the media items of a specific type. Use the attribute name "MediaType" and one of the following values:

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>audio</td>
<td>Music and other audio-only items</td>
</tr>
<tr>
<td>other</td>
<td>Other items, such as an .asf file or the URL of a stream.</td>
</tr>
<tr>
<td>photo</td>
<td>Photo items. Requires Windows Media Player 10.</td>
</tr>
<tr>
<td>playlist</td>
<td>Playlists represented as media items.</td>
</tr>
<tr>
<td>radio</td>
<td>Radio station items. Not used by Windows Media Player 10.</td>
</tr>
<tr>
<td>video</td>
<td>Video items.</td>
</tr>
</table>
 

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByAttribute</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/en-us/library/Dd563231(v=VS.85).aspx">IWMPCore::get_mediaCollection</a>, then the <b>getByAttribute</b> method returns all the media items in the library that have the specified attribute and value. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/en-us/library/Dd563392(v=VS.85).aspx">IWMPLibrary::get_mediaCollection</a>, then the <b>getByAttribute</b> method returns only the audio items in the library that have the specified attribute and value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563405(v=VS.85).aspx">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563553(v=VS.85).aspx">IWMPPlaylistCollection::getAll</a>
 

 

