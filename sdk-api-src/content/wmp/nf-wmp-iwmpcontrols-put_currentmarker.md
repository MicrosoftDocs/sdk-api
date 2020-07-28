---
UID: NF:wmp.IWMPControls.put_currentMarker
title: IWMPControls::put_currentMarker (wmp.h)
description: The put_currentMarker method specifies the current marker number.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","put_currentMarker method","IWMPControls.put_currentMarker","IWMPControls::put_currentMarker","IWMPControlsput_currentMarker","put_currentMarker","put_currentMarker method [Windows Media Player]","put_currentMarker method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_put_currentmarker","wmp/IWMPControls::put_currentMarker"]
old-location: wmp\iwmpcontrols_put_currentmarker.htm
tech.root: WMP
ms.assetid: b48e50b3-46d2-4994-bbbf-668f4986109a
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],put_currentMarker method, IWMPControls.put_currentMarker, IWMPControls::put_currentMarker, IWMPControlsput_currentMarker, put_currentMarker, put_currentMarker method [Windows Media Player], put_currentMarker method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentmarker, wmp/IWMPControls::put_currentMarker
f1_keywords:
- wmp/IWMPControls.put_currentMarker
dev_langs:
- c++
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
- IWMPControls.put_currentMarker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls::put_currentMarker


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentmarker">IWMPControls::get_currentMarker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">IWMPCore::put_currentMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_markercount">IWMPMedia::get_markerCount</a>
 

 

