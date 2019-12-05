---
UID: NF:strmif.IDvdInfo2.GetCurrentLocation
title: IDvdInfo2::GetCurrentLocation (strmif.h)
description: The GetCurrentLocation method retrieves the current playback location.
old-location: dshow\idvdinfo2_getcurrentlocation.htm
tech.root: DirectShow
ms.assetid: 54005c07-1689-411c-88a9-bcd19cc065dd
ms.date: 12/05/2018
ms.keywords: GetCurrentLocation, GetCurrentLocation method [DirectShow], GetCurrentLocation method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentLocation method, IDvdInfo2.GetCurrentLocation, IDvdInfo2::GetCurrentLocation, IDvdInfo2GetCurrentLocation, dshow.idvdinfo2_getcurrentlocation, strmif/IDvdInfo2::GetCurrentLocation
ms.topic: method
f1_keywords:
- strmif/IDvdInfo2.GetCurrentLocation
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdInfo2.GetCurrentLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetCurrentLocation


## -description



The <code>GetCurrentLocation</code> method retrieves the current playback location.




## -parameters




### -param pLocation [out]

Pointer to a variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_playback_location2">DVD_PLAYBACK_LOCATION2</a> that receives the playback location information.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pLocation</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is in an invalid domain.

</td>
</tr>
</table>
 




## -remarks



This method retrieves information sufficient to restart playback of a video from the current playback location in titles that don't explicitly disable seeking to the current location. After the disc has been ejected, the information returned by this method will not necessarily be sufficient to restart playback. To save the current location and state information to disc so that the user can return to the same location at any later time, use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">GetState</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

