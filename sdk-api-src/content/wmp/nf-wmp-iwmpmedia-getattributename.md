---
UID: NF:wmp.IWMPMedia.getAttributeName
title: IWMPMedia::getAttributeName
author: windows-driver-content
description: The getAttributeName method retrieves the name of the attribute corresponding to the specified index.
old-location: wmp\iwmpmedia_getattributename.htm
old-project: WMP
ms.assetid: cb04e464-44dd-41ba-9296-f13aca9ef54e
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPMedia interface [Windows Media Player],getAttributeName method, IWMPMedia.getAttributeName, IWMPMedia2 interface [Windows Media Player],getAttributeName method, IWMPMedia2::getAttributeName, IWMPMedia3 interface [Windows Media Player],getAttributeName method, IWMPMedia3::getAttributeName, IWMPMedia::getAttributeName, IWMPMediagetAttributeName, getAttributeName, getAttributeName method [Windows Media Player], getAttributeName method [Windows Media Player],IWMPMedia interface, getAttributeName method [Windows Media Player],IWMPMedia2 interface, getAttributeName method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getattributename, wmp/IWMPMedia2::getAttributeName, wmp/IWMPMedia3::getAttributeName, wmp/IWMPMedia::getAttributeName
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
-	IWMPMedia.getAttributeName
-	IWMPMedia2.getAttributeName
-	IWMPMedia3.getAttributeName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::getAttributeName


## -description



The <b>getAttributeName</b> method retrieves the name of the attribute corresponding to the specified index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param pbstrItemName [out]

Pointer to a <b>BSTR</b> containing the attribute name.


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



The attribute name returned can be used in conjunction with <b>getItemInfo</b> to retrieve the value for a specific named attribute.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a>
 

 

