---
UID: NF:strmif.IDvdInfo.GetCurrentLocation
title: IDvdInfo::GetCurrentLocation (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current playback location.
helpviewer_keywords: ["GetCurrentLocation","GetCurrentLocation method [DirectShow]","GetCurrentLocation method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentLocation method","IDvdInfo.GetCurrentLocation","IDvdInfo::GetCurrentLocation","IDvdInfoGetCurrentLocation","dshow.idvdinfo_getcurrentlocation","strmif/IDvdInfo::GetCurrentLocation"]
old-location: dshow\idvdinfo_getcurrentlocation.htm
tech.root: dshow
ms.assetid: 27913630-d0c2-4bc1-9d6a-623f7aa631ec
ms.date: 12/05/2018
ms.keywords: GetCurrentLocation, GetCurrentLocation method [DirectShow], GetCurrentLocation method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentLocation method, IDvdInfo.GetCurrentLocation, IDvdInfo::GetCurrentLocation, IDvdInfoGetCurrentLocation, dshow.idvdinfo_getcurrentlocation, strmif/IDvdInfo::GetCurrentLocation
f1_keywords:
- strmif/IDvdInfo.GetCurrentLocation
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IDvdInfo.GetCurrentLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetCurrentLocation


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current playback location.




## -parameters




### -param pLocation [out]

Pointer to the retrieved playback location information in a [DVD_PLAYBACK_LOCATION](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_playback_location) structure.


## -returns



Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>
 




## -remarks



This method retrieves information sufficient to restart playback of a video from the current playback location in titles that don't explicitly disable seeking to the current location.

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

