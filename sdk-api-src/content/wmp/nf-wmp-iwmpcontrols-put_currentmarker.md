---
UID: NF:wmp.IWMPControls.put_currentMarker
title: IWMPControls::put_currentMarker method
author: windows-driver-content
description: The put_currentMarker method specifies the current marker number.
old-location: wmp\iwmpcontrols_put_currentmarker.htm
old-project: WMP
ms.assetid: b48e50b3-46d2-4994-bbbf-668f4986109a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPControls, IWMPControls interface [Windows Media Player], put_currentMarker method, IWMPControls::put_currentMarker, IWMPControlsput_currentMarker, put_currentMarker method [Windows Media Player], put_currentMarker method [Windows Media Player], IWMPControls interface, put_currentMarker,IWMPControls.put_currentMarker, wmp.iwmpcontrols_put_currentmarker, wmp/IWMPControls::put_currentMarker
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
-	IWMPControls.put_currentMarker
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::put_currentMarker method


## -description



The <b>put_currentMarker</b> method specifies the current marker number.




## -parameters




### -param lMarker [in]

<b>long</b> containing the marker.


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



Specifying a marker with the <b>put_currentMarker</b> method causes playback to start from that marker. Before attempting to specify a marker with <b>put_currentMarker</b>, determine whether a file has markers and how many it has by calling <b>IWMPMedia::get_markerCount</b>. If a file has no markers, specifying a marker to anything but zero by using <b>put_currentMarker</b> results in an error. Specifying a marker to a number higher than a number retrieved by using <b>IWMPMedia::get_markerCount</b> also results in an error.

Until the current media item is set (using <b>IWMPCore::put_URL</b> or <b>IWMPCore::put_currentMedia</b>), <b>get_currentMarker</b> retrieves a marker that is zero.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/42576961-a9bd-4f64-bf56-a5d6bd07e82f">IWMPControls::get_currentMarker</a>



<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">IWMPCore::put_currentMedia</a>



<a href="https://msdn.microsoft.com/e97c8d26-fa6a-4791-a698-b742eaf980eb">IWMPMedia::get_markerCount</a>
 

 

