---
UID: NF:wmp.IWMPMedia.getMarkerTime
title: IWMPMedia::getMarkerTime
author: windows-sdk-content
description: The getMarkerTime method retrieves the time of the marker at the specified index.
old-location: wmp\iwmpmedia_getmarkertime.htm
old-project: WMP
ms.assetid: e6c2484d-8167-4305-9467-f9b2b7fedc32
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPMedia interface [Windows Media Player],getMarkerTime method, IWMPMedia.getMarkerTime, IWMPMedia2 interface [Windows Media Player],getMarkerTime method, IWMPMedia2::getMarkerTime, IWMPMedia3 interface [Windows Media Player],getMarkerTime method, IWMPMedia3::getMarkerTime, IWMPMedia::getMarkerTime, IWMPMediagetMarkerTime, getMarkerTime, getMarkerTime method [Windows Media Player], getMarkerTime method [Windows Media Player],IWMPMedia interface, getMarkerTime method [Windows Media Player],IWMPMedia2 interface, getMarkerTime method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getmarkertime, wmp/IWMPMedia2::getMarkerTime, wmp/IWMPMedia3::getMarkerTime, wmp/IWMPMedia::getMarkerTime
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
 - IWMPMedia.getMarkerTime
 - IWMPMedia2.getMarkerTime
 - IWMPMedia3.getMarkerTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::getMarkerTime


## -description



The <b>getMarkerTime</b> method retrieves the time of the marker at the specified index.




## -parameters




### -param MarkerNum [in]

<b>long</b> specifying the marker index.


### -param pMarkerTime [out]

Pointer to a <b>double</b> that specifies the marker time.


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



This method returns <b>NULL</b> if the specified marker does not exist.

Some media items do not contain markers. Use <b>get_markerCount</b> to find out how many markers are in the current media item.

Marker index numbers start at 1.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/e97c8d26-fa6a-4791-a698-b742eaf980eb">IWMPMedia::get_markerCount</a>
 

 

