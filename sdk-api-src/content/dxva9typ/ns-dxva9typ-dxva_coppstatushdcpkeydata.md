---
UID: NS:dxva9typ._DXVA_COPPStatusHDCPKeyData
title: DXVA_COPPStatusHDCPKeyData (dxva9typ.h)
description: Contains the result from an HDCP Key Data query in Certified Output Protection Protocol (COPP). This query returns the device's HDCP key selection vector (KSV).
helpviewer_keywords: ["DXVA_COPPStatusHDCPKeyData","DXVA_COPPStatusHDCPKeyData structure [DirectShow]","DXVA_COPPStatusHDCPKeyDataStructure","_DXVA_COPPStatusHDCPKeyData","dshow.dxva_coppstatushdcpkeydata","dxva9typ/DXVA_COPPStatusHDCPKeyData"]
old-location: dshow\dxva_coppstatushdcpkeydata.htm
tech.root: dshow
ms.assetid: fd49c50d-6caa-4d2a-83c6-41ff0130160f
ms.date: 4/26/2023
ms.keywords: DXVA_COPPStatusHDCPKeyData, DXVA_COPPStatusHDCPKeyData structure [DirectShow], DXVA_COPPStatusHDCPKeyDataStructure, _DXVA_COPPStatusHDCPKeyData, dshow.dxva_coppstatushdcpkeydata, dxva9typ/DXVA_COPPStatusHDCPKeyData
req.header: dxva9typ.h
req.include-header: Dxva.h
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
req.typenames: DXVA_COPPStatusHDCPKeyData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA_COPPStatusHDCPKeyData
 - dxva9typ/_DXVA_COPPStatusHDCPKeyData
 - DXVA_COPPStatusHDCPKeyData
 - dxva9typ/DXVA_COPPStatusHDCPKeyData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVA_COPPStatusHDCPKeyData
---

# DXVA_COPPStatusHDCPKeyData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains the result from an HDCP Key Data query in Certified Output Protection Protocol (COPP). This query returns the device's HDCP key selection vector (KSV).

## -struct-fields

### -field rApp

A 128-bit random number that was passed by the application in the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppstatusinput">AMCOPPStatusInput</a> structure.

### -field dwFlags

Status flag. See <a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags">COPP_StatusFlags</a>.

### -field dwHDCPFlags

Receives zero or more flags from the <a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statushdcpflags">COPP_StatusHDCPFlags</a> enumeration. If the COPP_HDCPRepeater flag is present, the application should not play the content using this graphics adapter.

### -field BKey

Receives the HDCP key selection vector, B<sub>KSV</sub>, from the HDSCP device attached to the graphics adapter.

### -field Reserved1

Reserved. Must be zero.

### -field Reserved2

Reserved. Must be zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>