---
UID: NF:wmp.IWMPMedia.get_markerCount
title: IWMPMedia::get_markerCount
author: windows-driver-content
description: The get_markerCount method retrieves the number of markers in the media item.
old-location: wmp\iwmpmedia_get_markercount.htm
old-project: WMP
ms.assetid: e97c8d26-fa6a-4791-a698-b742eaf980eb
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_markerCount method, IWMPMedia.get_markerCount, IWMPMedia2 interface [Windows Media Player],get_markerCount method, IWMPMedia2::get_markerCount, IWMPMedia3 interface [Windows Media Player],get_markerCount method, IWMPMedia3::get_markerCount, IWMPMedia::get_markerCount, IWMPMediaget_markerCount, get_markerCount, get_markerCount method [Windows Media Player], get_markerCount method [Windows Media Player],IWMPMedia interface, get_markerCount method [Windows Media Player],IWMPMedia2 interface, get_markerCount method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_markercount, wmp/IWMPMedia2::get_markerCount, wmp/IWMPMedia3::get_markerCount, wmp/IWMPMedia::get_markerCount
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
-	IWMPMedia.get_markerCount
-	IWMPMedia2.get_markerCount
-	IWMPMedia3.get_markerCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::get_markerCount


## -description



The <b>get_markerCount</b> method retrieves the number of markers in the media item.




## -parameters




### -param pMarkerCount [out]

Pointer to a <b>long</b> that contains the marker count.


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



This method returns zero if a file has no markers, or if the media item is not the same as the one specified in <b>IWMPCore::get_currentMedia</b>.

Marker numbers start at 1.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f199336-0555-40de-8d27-780b05ef9510">IWMPCore::get_currentMedia</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>
 

 

