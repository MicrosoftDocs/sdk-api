---
UID: NF:segment.IMSVidAudioRendererDevices.get_Count
title: IMSVidAudioRendererDevices::get_Count (segment.h)
description: The get_Count method retrieves the number of items in the collection.
helpviewer_keywords: ["IMSVidAudioRendererDevices interface [Microsoft TV Technologies]","get_Count method","IMSVidAudioRendererDevices.get_Count","IMSVidAudioRendererDevices::get_Count","IMSVidAudioRendererDevicesget_Count","get_Count","get_Count method [Microsoft TV Technologies]","get_Count method [Microsoft TV Technologies]","IMSVidAudioRendererDevices interface","mstv.imsvidaudiorendererdevices_get_count","segment/IMSVidAudioRendererDevices::get_Count"]
old-location: mstv\imsvidaudiorendererdevices_get_count.htm
tech.root: mstv
ms.assetid: 46a3b579-a027-4c80-9f7a-f81dd9af4d0d
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRendererDevices interface [Microsoft TV Technologies],get_Count method, IMSVidAudioRendererDevices.get_Count, IMSVidAudioRendererDevices::get_Count, IMSVidAudioRendererDevicesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IMSVidAudioRendererDevices interface, mstv.imsvidaudiorendererdevices_get_count, segment/IMSVidAudioRendererDevices::get_Count
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidAudioRendererDevices::get_Count
 - segment/IMSVidAudioRendererDevices::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidAudioRendererDevices.get_Count
---

# IMSVidAudioRendererDevices::get_Count


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Count</b> method retrieves the number of items in the collection.

## -parameters

### -param lCount [out]

Pointer to a variable that receives the number of items.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidaudiorendererdevices">IMSVidAudioRendererDevices Interface</a>