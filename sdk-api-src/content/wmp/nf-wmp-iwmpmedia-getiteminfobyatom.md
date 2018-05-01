---
UID: NF:wmp.IWMPMedia.getItemInfoByAtom
title: IWMPMedia::getItemInfoByAtom method
author: windows-driver-content
description: The getItemInfoByAtom method retrieves the value of the attribute with the specified index number.
old-location: wmp\iwmpmedia_getiteminfobyatom.htm
old-project: WMP
ms.assetid: c2e803df-84f2-4c23-9872-a5435977d189
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], getItemInfoByAtom method, IWMPMedia2 interface [Windows Media Player], getItemInfoByAtom method, IWMPMedia2::getItemInfoByAtom, IWMPMedia3 interface [Windows Media Player], getItemInfoByAtom method, IWMPMedia3::getItemInfoByAtom, IWMPMedia::getItemInfoByAtom, IWMPMediagetItemInfoByAtom, getItemInfoByAtom method [Windows Media Player], getItemInfoByAtom method [Windows Media Player], IWMPMedia interface, getItemInfoByAtom method [Windows Media Player], IWMPMedia2 interface, getItemInfoByAtom method [Windows Media Player], IWMPMedia3 interface, getItemInfoByAtom,IWMPMedia.getItemInfoByAtom, wmp.iwmpmedia_getiteminfobyatom, wmp/IWMPMedia2::getItemInfoByAtom, wmp/IWMPMedia3::getItemInfoByAtom, wmp/IWMPMedia::getItemInfoByAtom
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPMedia.getItemInfoByAtom
-	IWMPMedia2.getItemInfoByAtom
-	IWMPMedia3.getItemInfoByAtom
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::getItemInfoByAtom method


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




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/2a77029b-fbae-49af-bd91-c688c11b3b16">IWMPMedia3::getItemInfoByType</a>



<a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a>



<a href="https://msdn.microsoft.com/33e29da2-7439-41d1-9dd9-9b66e87aeb4b">IWMPMedia::get_attributeCount</a>



<a href="https://msdn.microsoft.com/919fe92f-9519-4229-8097-4970a8f6cc25">IWMPMedia::setItemInfo</a>



<a href="https://msdn.microsoft.com/22024108-398e-4a05-b5ed-311583c69497">IWMPMediaCollection::getMediaAtom</a>
 

 

