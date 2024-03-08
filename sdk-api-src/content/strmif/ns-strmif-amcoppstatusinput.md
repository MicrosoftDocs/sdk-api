---
UID: NS:strmif._AMCOPPStatusInput
title: AMCOPPStatusInput (strmif.h)
description: The AMCOPPStatusInput structure contains a Certified Output Protection Protocol (COPP) status request.
helpviewer_keywords: ["*LPAMCOPPStatusInput","AMCOPPStatusInput","AMCOPPStatusInput structure [DirectShow]","AMCOPPStatusInputStructure","LPAMCOPPStatusInput","LPAMCOPPStatusInput structure pointer [DirectShow]","dshow.amcoppstatusinput","strmif/AMCOPPStatusInput","strmif/LPAMCOPPStatusInput"]
old-location: dshow\amcoppstatusinput.htm
tech.root: dshow
ms.assetid: 988e6d54-f241-4cfc-8793-fc42de92ac52
ms.date: 4/26/2023
ms.keywords: '*LPAMCOPPStatusInput, AMCOPPStatusInput, AMCOPPStatusInput structure [DirectShow], AMCOPPStatusInputStructure, LPAMCOPPStatusInput, LPAMCOPPStatusInput structure pointer [DirectShow], dshow.amcoppstatusinput, strmif/AMCOPPStatusInput, strmif/LPAMCOPPStatusInput'
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
targetos: Windows
req.typenames: AMCOPPStatusInput, *LPAMCOPPStatusInput
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMCOPPStatusInput
 - strmif/_AMCOPPStatusInput
 - LPAMCOPPStatusInput
 - strmif/LPAMCOPPStatusInput
 - AMCOPPStatusInput
 - strmif/AMCOPPStatusInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AMCOPPStatusInput
---

# AMCOPPStatusInput structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The AMCOPPStatusInput structure contains a Certified Output Protection Protocol (COPP) status request.

## -struct-fields

### -field rApp

128-bit random number.

### -field guidStatusRequestID

GUID that defines the status request.

### -field dwSequence

Sequence number. The application must keep a running count of the COPP status requests issued. For each request, increment the sequence number by one.

### -field cbSizeData

Number of bytes of valid data in the <b>StatusData</b> member.

### -field StatusData

Data for the status request. The meaning of the data depends on the request.

## -remarks

The following COPP status requests are defined.

<table>
<tr>
<th><b>GUID</b></th>
<th>Description
            </th>
</tr>
<tr>
<td><b>DXVA_COPPQueryConnectorType</b></td>
<td>Returns the type of physical connector to the output device.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryProtectionType</b></td>
<td>Returns the available protection mechanisms for the physical connector.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryLocalProtectionLevel</b></td>
<td>Returns the protection level that is currently set through the COPP mechanism in the context of this session.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryGlobalProtectionLevel</b></td>
<td>Returns the actual protection level that is currently set for the physical connector.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryDisplayData</b></td>
<td>Returns information describing the signal that is being transmitted over the connector associated with the COPP device.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryHDCPKeyData</b></td>
<td>Returns the High-bandwidth Digital Content Protection (HDCP) characteristics of the output device.</td>
</tr>
<tr>
<td><b>DXVA_COPPQueryBusData</b></td>
<td>Returns information about the type of bus used by the graphics hardware associated with this COPP device.</td>
</tr>
</table>
 

For more information, see the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>