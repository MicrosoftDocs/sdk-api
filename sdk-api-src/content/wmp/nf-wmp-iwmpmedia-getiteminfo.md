---
UID: NF:wmp.IWMPMedia.getItemInfo
title: IWMPMedia::getItemInfo
author: windows-sdk-content
description: The getItemInfo method retrieves the value of the specified attribute for the media item.
old-location: wmp\iwmpmedia_getiteminfo.htm
old-project: WMP
ms.assetid: ee964f68-d44c-4e66-908b-09070a96d96f
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPMedia interface [Windows Media Player],getItemInfo method, IWMPMedia.getItemInfo, IWMPMedia2 interface [Windows Media Player],getItemInfo method, IWMPMedia2::getItemInfo, IWMPMedia3 interface [Windows Media Player],getItemInfo method, IWMPMedia3::getItemInfo, IWMPMedia::getItemInfo, IWMPMediagetItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPMedia interface, getItemInfo method [Windows Media Player],IWMPMedia2 interface, getItemInfo method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getiteminfo, wmp/IWMPMedia2::getItemInfo, wmp/IWMPMedia3::getItemInfo, wmp/IWMPMedia::getItemInfo
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
 - IWMPMedia.getItemInfo
 - IWMPMedia2.getItemInfo
 - IWMPMedia3.getItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::getItemInfo


## -description



The <b>getItemInfo</b> method retrieves the value of the specified attribute for the media item.




## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the item name.


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



This method retrieves the metadata for an individual media item or a media item that is part of a playlist.

The <b>get_attributeCount</b> method retrieves the number of attribute names available for a given media item. Index numbers can then be used with the <b>getAttributeName</b> method to determine the name of each available attribute. Individual attribute names can be passed to <b>getItemInfo</b>.

To retrieve attributes with multiple values and attributes with complex values, use the <b>getItemInfoByType</b> method.

The set of attributes available from sources other than the local library (remote libraries, portable devices, or CDs) is defined by the other sources.

Before calling this method, you must have Read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that 

is exposed over UPnP. Other devices can then navigate and browse the libraries. 


In Windows 7, an application can use the Windows Media Player <a href="https://msdn.microsoft.com/77afa1a5-d532-4b54-9308-a274c5c7bdde">TrackingID</a> and <a href="https://msdn.microsoft.com/0d8a6937-32d8-4a4a-87e5-0002f077fefe">MediaType</a> attributes to construct the object ID of each item in the CDS. Note that this construction might change in future versions of Windows. The application passes each of these attribute strings in the <i>bstrItemName</i> parameter in a call to <b>getItemInfo</b>. <b>getItemInfo</b> returns the value for each attribute in a variable to which the   <i>pbstrVal</i> parameter points.  The application then uses the following syntax to construct each object ID:

<i>TrackingID</i>.0.<i>MediaTypeID</i>

This syntax has the  following meaning:

<ul>
<li><i>TrackingID</i> is the string that is stored in the Windows Media Player <a href="https://msdn.microsoft.com/77afa1a5-d532-4b54-9308-a274c5c7bdde">TrackingID</a> attribute of the media item.</li>
<li><i>MediaTypeID</i> depends on the value of the <a href="https://msdn.microsoft.com/0d8a6937-32d8-4a4a-87e5-0002f077fefe">MediaType</a> 

attribute, as shown in the following table:<table>
<tr>
<th>MediaType attribute</th>
<th>MediaTypeID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fbaff235-47bb-4fa2-8961-53dac26142dd">Audio Items</a>
</td>
<td>4</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3d3ed3a8-09ac-4e3d-b52d-3614b3a3fc05">Photo Items</a>
</td>
<td>B</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/000bc03d-aa2e-4922-b611-7d6e8ebb22e9">Video Items</a>
</td>
<td>8</td>
</tr>
</table>
 

</li>
</ul>
<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.




## -see-also




<a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/2a77029b-fbae-49af-bd91-c688c11b3b16">IWMPMedia3::getItemInfoByType</a>



<a href="https://msdn.microsoft.com/cb04e464-44dd-41ba-9296-f13aca9ef54e">IWMPMedia::getAttributeName</a>



<a href="https://msdn.microsoft.com/33e29da2-7439-41d1-9dd9-9b66e87aeb4b">IWMPMedia::get_attributeCount</a>



<a href="https://msdn.microsoft.com/919fe92f-9519-4229-8097-4970a8f6cc25">IWMPMedia::setItemInfo</a>
 

 

