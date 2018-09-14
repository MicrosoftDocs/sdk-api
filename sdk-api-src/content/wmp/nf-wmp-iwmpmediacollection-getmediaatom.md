---
UID: NF:wmp.IWMPMediaCollection.getMediaAtom
title: IWMPMediaCollection::getMediaAtom
author: windows-sdk-content
description: The getMediaAtom method retrieves the index at which a given attribute resides within the set of available attributes.
old-location: wmp\iwmpmediacollection_getmediaatom.htm
tech.root: WMP
ms.assetid: 22024108-398e-4a05-b5ed-311583c69497
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getMediaAtom method, IWMPMediaCollection.getMediaAtom, IWMPMediaCollection::getMediaAtom, IWMPMediaCollectiongetMediaAtom, getMediaAtom, getMediaAtom method [Windows Media Player], getMediaAtom method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getmediaatom, wmp/IWMPMediaCollection::getMediaAtom
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
 - IWMPMediaCollection.getMediaAtom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection::getMediaAtom


## -description



The <b>getMediaAtom</b> method retrieves the index at which a given attribute resides within the set of available attributes.




## -parameters




### -param bstrItemName [in]

String containing the name of the item for which the index should be retrieved.


### -param plAtom [out]

Pointer to a <b>long</b> containing the index.


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



The index number retrieved with this method can be passed to the <b>IWMPMedia::getItemInfoByAtom</b> to access attribute values. This technique is generally more efficient when working with large playlists than accessing an attribute value by name through <b>IWMPMedia::getItemInfo</b>.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a>



<a href="https://msdn.microsoft.com/c2e803df-84f2-4c23-9872-a5435977d189">IWMPMedia::getItemInfoByAtom</a>



<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>
 

 

