---
UID: NS:dxva9typ._DXVA_COPPStatusData
title: DXVA_COPPStatusData (dxva9typ.h)
description: Contains the result from a Certified Output Protection Protocol (COPP) status request.
helpviewer_keywords: ["DXVA_COPPStatusData","DXVA_COPPStatusData structure [DirectShow]","DXVA_COPPStatusDataStructure","_DXVA_COPPStatusData","dshow.dxva_coppstatusdata","dxva9typ/DXVA_COPPStatusData"]
old-location: dshow\dxva_coppstatusdata.htm
tech.root: dshow
ms.assetid: 62172141-cda4-4713-8ae2-e1f0c5f3fba8
ms.date: 4/26/2023
ms.keywords: DXVA_COPPStatusData, DXVA_COPPStatusData structure [DirectShow], DXVA_COPPStatusDataStructure, _DXVA_COPPStatusData, dshow.dxva_coppstatusdata, dxva9typ/DXVA_COPPStatusData
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
req.typenames: DXVA_COPPStatusData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA_COPPStatusData
 - dxva9typ/_DXVA_COPPStatusData
 - DXVA_COPPStatusData
 - dxva9typ/DXVA_COPPStatusData
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
 - DXVA_COPPStatusData
---

# DXVA_COPPStatusData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains the result from a Certified Output Protection Protocol (COPP) status request.

## -struct-fields

### -field rApp

A 128-bit random number that was passed by the application in the <a href="/windows/desktop/api/strmif/ns-strmif-amcoppstatusinput">AMCOPPStatusInput</a> structure.

### -field dwFlags

Status flag. See <a href="/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags">COPP_StatusFlags</a>.

### -field dwData

Response to the status query. The meaning of this value depends on the status request. For more information, see <a href="/windows/desktop/DirectShow/copp-query-reference">COPP Query Reference</a>.

### -field ExtendedInfoValidMask

Reserved. Must be zero.

### -field ExtendedInfoData

Reserved. Must be zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>