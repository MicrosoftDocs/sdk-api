---
UID: NF:segment.IMSVidVideoRendererDevices.Add
title: IMSVidVideoRendererDevices::Add (segment.h)
description: The Add method adds a video renderer to the collection.
helpviewer_keywords: ["Add","Add method [Microsoft TV Technologies]","Add method [Microsoft TV Technologies]","IMSVidVideoRendererDevices interface","IMSVidVideoRendererDevices interface [Microsoft TV Technologies]","Add method","IMSVidVideoRendererDevices.Add","IMSVidVideoRendererDevices::Add","IMSVidVideoRendererDevicesAdd","mstv.imsvidvideorendererdevices_add","segment/IMSVidVideoRendererDevices::Add"]
old-location: mstv\imsvidvideorendererdevices_add.htm
tech.root: mstv
ms.assetid: 650b7895-4e4b-494a-bc06-dafb67fca391
ms.date: 12/05/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, IMSVidVideoRendererDevices interface [Microsoft TV Technologies],Add method, IMSVidVideoRendererDevices.Add, IMSVidVideoRendererDevices::Add, IMSVidVideoRendererDevicesAdd, mstv.imsvidvideorendererdevices_add, segment/IMSVidVideoRendererDevices::Add
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
 - IMSVidVideoRendererDevices::Add
 - segment/IMSVidVideoRendererDevices::Add
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
 - IMSVidVideoRendererDevices.Add
---

# IMSVidVideoRendererDevices::Add


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Add</b> method adds a video renderer to the collection.

## -parameters

### -param pDB [in]

Specifies a pointer to the video renderer's <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only; cannot add any items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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

<a href="/previous-versions/windows/desktop/mstv/msvidvideorendererdevices">IMSVidVideoRendererDevices Interface</a>