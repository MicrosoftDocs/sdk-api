---
UID: NF:wmp.IWMPMedia.getItemInfoByAtom
title: IWMPMedia::getItemInfoByAtom
author: windows-sdk-content
description: The getItemInfoByAtom method retrieves the value of the attribute with the specified index number.
old-location: wmp\iwmpmedia_getiteminfobyatom.htm
tech.root: WMP
ms.assetid: c2e803df-84f2-4c23-9872-a5435977d189
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMedia interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia.getItemInfoByAtom, IWMPMedia2 interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia2::getItemInfoByAtom, IWMPMedia3 interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia3::getItemInfoByAtom, IWMPMedia::getItemInfoByAtom, IWMPMediagetItemInfoByAtom, getItemInfoByAtom, getItemInfoByAtom method [Windows Media Player], getItemInfoByAtom method [Windows Media Player],IWMPMedia interface, getItemInfoByAtom method [Windows Media Player],IWMPMedia2 interface, getItemInfoByAtom method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getiteminfobyatom, wmp/IWMPMedia2::getItemInfoByAtom, wmp/IWMPMedia3::getItemInfoByAtom, wmp/IWMPMedia::getItemInfoByAtom
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
 - IWMPMedia.getItemInfoByAtom
 - IWMPMedia2.getItemInfoByAtom
 - IWMPMedia3.getItemInfoByAtom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMedia::getItemInfoByAtom


## -description



The <b>getItemInfoByAtom</b> method retrieves the value of the attribute with the specified index number.




## -parameters




### -param lAtom [in]

<b>long</b> specifying the index at which a given attribute resides within the set of available attributes.


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> containing the returned value.


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



This method can be used to retrieve metadata for a specific media item by using an attribute index number. The <b>get_attributeCount</b> method can be used to determine the number of attributes available for the media item.

The <b>getMediaAtom</b> method of the <b>MediaCollection</b> object can also be used to retrieve the index of a particular attribute. This technique is generally more efficient than the <b>getItemInfo</b> or <b>getItemInfoByType</b> methods when working with large playlists.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563397(v=VS.85).aspx">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563403(v=VS.85).aspx">IWMPMedia3::getItemInfoByType</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563431(v=VS.85).aspx">IWMPMedia::getItemInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563435(v=VS.85).aspx">IWMPMedia::get_attributeCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563449(v=VS.85).aspx">IWMPMedia::setItemInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563420(v=VS.85).aspx">IWMPMediaCollection::getMediaAtom</a>
 

 

