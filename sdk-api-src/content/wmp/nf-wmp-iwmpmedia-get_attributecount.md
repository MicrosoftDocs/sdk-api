---
UID: NF:wmp.IWMPMedia.get_attributeCount
title: IWMPMedia::get_attributeCount
author: windows-sdk-content
description: The get_attributeCount method retrieves the number of attributes that can be queried and/or set for the media item.
old-location: wmp\iwmpmedia_get_attributecount.htm
tech.root: WMP
ms.assetid: 33e29da2-7439-41d1-9dd9-9b66e87aeb4b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_attributeCount method, IWMPMedia.get_attributeCount, IWMPMedia2 interface [Windows Media Player],get_attributeCount method, IWMPMedia2::get_attributeCount, IWMPMedia3 interface [Windows Media Player],get_attributeCount method, IWMPMedia3::get_attributeCount, IWMPMedia::get_attributeCount, IWMPMediaget_attributeCount, get_attributeCount, get_attributeCount method [Windows Media Player], get_attributeCount method [Windows Media Player],IWMPMedia interface, get_attributeCount method [Windows Media Player],IWMPMedia2 interface, get_attributeCount method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_attributecount, wmp/IWMPMedia2::get_attributeCount, wmp/IWMPMedia3::get_attributeCount, wmp/IWMPMedia::get_attributeCount
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
 - IWMPMedia.get_attributeCount
 - IWMPMedia2.get_attributeCount
 - IWMPMedia3.get_attributeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMedia::get_attributeCount


## -description



The <b>get_attributeCount</b> method retrieves the number of attributes that can be queried and/or set for the media item.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> containing the count.


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

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>
 

 

