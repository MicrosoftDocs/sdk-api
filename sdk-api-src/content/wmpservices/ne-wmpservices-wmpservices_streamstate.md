---
UID: NE:wmpservices.WMPServices_StreamState
title: WMPServices_StreamState (wmpservices.h)
description: The WMPServices_StreamState enumeration indicates whether the stream is currently stopped, paused, or playing.
helpviewer_keywords: ["WMPServices_StreamState","WMPServices_StreamState enumeration [Windows Media Player]","WMPServices_StreamStateDSP","WMPServices_StreamState_Pause","WMPServices_StreamState_Play","WMPServices_StreamState_Stop","wmp.wmpservices_streamstate","wmpservices/WMPServices_StreamState","wmpservices/WMPServices_StreamState_Pause","wmpservices/WMPServices_StreamState_Play","wmpservices/WMPServices_StreamState_Stop"]
old-location: wmp\wmpservices_streamstate.htm
tech.root: WMP
ms.assetid: 82c4699a-197c-4429-afa8-b1fc47a1f47a
ms.date: 12/05/2018
ms.keywords: WMPServices_StreamState, WMPServices_StreamState enumeration [Windows Media Player], WMPServices_StreamStateDSP, WMPServices_StreamState_Pause, WMPServices_StreamState_Play, WMPServices_StreamState_Stop, wmp.wmpservices_streamstate, wmpservices/WMPServices_StreamState, wmpservices/WMPServices_StreamState_Pause, wmpservices/WMPServices_StreamState_Play, wmpservices/WMPServices_StreamState_Stop
req.header: wmpservices.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMPServices_StreamState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPServices_StreamState
 - wmpservices/WMPServices_StreamState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpservices.h
api_name:
 - WMPServices_StreamState
---

# WMPServices_StreamState enumeration


## -description

The <b>WMPServices_StreamState</b> enumeration indicates whether the stream is currently stopped, paused, or playing.

## -enum-fields

### -field WMPServices_StreamState_Stop:0

The stream is stopped.

### -field WMPServices_StreamState_Pause

The stream is paused.

### -field WMPServices_StreamState_Play

The stream is playing.

## -see-also

<a href="/windows/desktop/WMP/dsp-plug-in-enumeration-types">DSP Plug-in Enumeration Types</a>



<a href="/windows/desktop/api/wmpservices/nf-wmpservices-iwmpservices-getstreamstate">IWMPServices::GetStreamState</a>
