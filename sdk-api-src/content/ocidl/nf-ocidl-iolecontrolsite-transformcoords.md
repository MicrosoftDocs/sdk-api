---
UID: NF:ocidl.IOleControlSite.TransformCoords
title: IOleControlSite::TransformCoords (ocidl.h)
description: Converts coordinates expressed in HIMETRIC units (as is standard in OLE) to the units specified by the container.
helpviewer_keywords: ["IOleControlSite interface [COM]","TransformCoords method","IOleControlSite.TransformCoords","IOleControlSite::TransformCoords","TransformCoords","TransformCoords method [COM]","TransformCoords method [COM]","IOleControlSite interface","XFORMCOORDS_CONTAINERTOHIMETRIC","XFORMCOORDS_EVENTCOMPAT","XFORMCOORDS_HIMETRICTOCONTAINER","XFORMCOORDS_POSITION","XFORMCOORDS_SIZE","_ctrl_iolecontrolsite_transformcoords","com.iolecontrolsite_transformcoords","ocidl/IOleControlSite::TransformCoords"]
old-location: com\iolecontrolsite_transformcoords.htm
tech.root: com
ms.assetid: c7add062-4b42-43be-a982-c881c947f8f0
ms.date: 12/05/2018
ms.keywords: IOleControlSite interface [COM],TransformCoords method, IOleControlSite.TransformCoords, IOleControlSite::TransformCoords, TransformCoords, TransformCoords method [COM], TransformCoords method [COM],IOleControlSite interface, XFORMCOORDS_CONTAINERTOHIMETRIC, XFORMCOORDS_EVENTCOMPAT, XFORMCOORDS_HIMETRICTOCONTAINER, XFORMCOORDS_POSITION, XFORMCOORDS_SIZE, _ctrl_iolecontrolsite_transformcoords, com.iolecontrolsite_transformcoords, ocidl/IOleControlSite::TransformCoords
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleControlSite::TransformCoords
 - ocidl/IOleControlSite::TransformCoords
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControlSite.TransformCoords
---

# IOleControlSite::TransformCoords


## -description

Converts coordinates expressed in <b>HIMETRIC</b> units (as is standard in OLE) to the units specified by the container.

## -parameters

### -param pPtlHimetric [in, out]

Address of a <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure containing coordinates expressed in <b>HIMETRIC</b> units. This is an [in] parameter when <i>dwFlags</i> contains XFORMCOORDS_HIMETRICTOCONTAINER; it is an [out] parameter with XFORMCOORDS_CONTAINERTOHIMETRIC. In the latter case, the contents are undefined on error.

### -param pPtfContainer [in, out]

Address of a caller-allocated <a href="/windows/desktop/api/ocidl/ns-ocidl-pointf">POINTF</a> structure that receives the converted coordinates. This is an [in] parameter when <i>dwFlags</i> contains XFORMCOORDS_CONTAINERTOHIMETRIC; it is an [out] parameter with XFORMCOORDS_HIMETRICTOCONTAINER. In the latter case, the contents are undefined on error.

### -param dwFlags [in]

Flags indicating the exact conversion to perform. This parameter can be any combination of the following values, except as indicated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XFORMCOORDS_POSITION"></a><a id="xformcoords_position"></a><dl>
<dt><b>XFORMCOORDS_POSITION</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The coordinates to convert represent a position point. Cannot be used with XFORMCOORDS_SIZE.


</td>
</tr>
<tr>
<td width="40%"><a id="XFORMCOORDS_SIZE"></a><a id="xformcoords_size"></a><dl>
<dt><b>XFORMCOORDS_SIZE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The coordinates to convert represent a set of dimensions. Cannot be used with XFORMCOORDS_POSITION.

</td>
</tr>
<tr>
<td width="40%"><a id="XFORMCOORDS_HIMETRICTOCONTAINER"></a><a id="xformcoords_himetrictocontainer"></a><dl>
<dt><b>XFORMCOORDS_HIMETRICTOCONTAINER</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The operation converts pptlHimetric into pptfContainer. Cannot be used with XFORMCOORDS_CONTAINERTOHIMETRIC.

</td>
</tr>
<tr>
<td width="40%"><a id="XFORMCOORDS_CONTAINERTOHIMETRIC"></a><a id="xformcoords_containertohimetric"></a><dl>
<dt><b>XFORMCOORDS_CONTAINERTOHIMETRIC</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The operation converts pptfContainer into pptlHimetric. Cannot be used with XFORMCOORDS_HIMETRICTOCONTAINER.

</td>
</tr>
<tr>
<td width="40%"><a id="XFORMCOORDS_EVENTCOMPAT"></a><a id="xformcoords_eventcompat"></a><dl>
<dt><b>XFORMCOORDS_EVENTCOMPAT</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The operation maintains compatibility with an event.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The container does not require any special coordinate conversions. The container deals completely in <b>HIMETRIC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pPtlHimetric</i> or <i>pPtfContainer</i> is not valid. For example, it may be <b>NULL</b>.


</td>
</tr>
</table>

## -remarks

A control uses this method when it has to send coordinates to a container within an event or some other custom call or when the control has container coordinates that it needs to convert into <b>HIMETRIC</b> units.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>