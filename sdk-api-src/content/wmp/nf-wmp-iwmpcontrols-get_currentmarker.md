---
UID: NF:wmp.IWMPControls.get_currentMarker
title: IWMPControls::get_currentMarker
author: windows-driver-content
description: The get_currentMarker method retrieves the current marker number.
old-location: wmp\iwmpcontrols_get_currentmarker.htm
old-project: WMP
ms.assetid: 42576961-a9bd-4f64-bf56-a5d6bd07e82f
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_currentMarker method, IWMPControls.get_currentMarker, IWMPControls::get_currentMarker, IWMPControlsget_currentMarker, get_currentMarker, get_currentMarker method [Windows Media Player], get_currentMarker method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentmarker, wmp/IWMPControls::get_currentMarker
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
-	IWMPControls.get_currentMarker
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::get_currentMarker


## -description



The <b>get_currentMarker</b> method retrieves the current marker number.




## -parameters




### -param plMarker [out]

Pointer to a <b>long</b> containing the marker.


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



The <b>get_currentMarker</b> method always retrieves a pointer to the current or last marker, which means the actual file position can be either at the current marker or before the next marker. Markers are numbered beginning at 1, so if a file has markers, you can change the current playback position to zero by calling <b>IWMPControls::put_currentMarker</b> to and specifying the marker as zero .

Until the current media item is set (using <b>IWMPCore::put_URL</b> or <b>IWMPCore::put_currentMedia</b>), <b>get_currentMarker</b> retrieves a marker that is zero.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/b48e50b3-46d2-4994-bbbf-668f4986109a">IWMPControls::put_currentMarker</a>



<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">IWMPCore::put_currentMedia</a>
 

 

