---
UID: NS:mmeapi.pcmwaveformat_tag
title: PCMWAVEFORMAT (mmeapi.h)
description: The PCMWAVEFORMAT structure describes the data format for PCM waveform-audio data. This structure has been superseded by the WAVEFORMATEX structure.
helpviewer_keywords: ["*LPPCMWAVEFORMAT","*NPPCMWAVEFORMAT","*PPCMWAVEFORMAT","PCMWAVEFORMAT","PCMWAVEFORMAT structure [Windows Multimedia]","_win32_PCMWAVEFORMAT_str","mmeapi/PCMWAVEFORMAT","multimedia.pcmwaveformat","pcmwaveformat_tag"]
old-location: multimedia\pcmwaveformat.htm
tech.root: Multimedia
ms.assetid: c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c
ms.date: 08/02/2022
ms.keywords: '*LPPCMWAVEFORMAT, *NPPCMWAVEFORMAT, *PPCMWAVEFORMAT, PCMWAVEFORMAT, PCMWAVEFORMAT structure [Windows Multimedia], _win32_PCMWAVEFORMAT_str, mmeapi/PCMWAVEFORMAT, multimedia.pcmwaveformat, pcmwaveformat_tag'
req.header: mmeapi.h
req.include-header: Mmreg.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PCMWAVEFORMAT, *PPCMWAVEFORMAT, *NPPCMWAVEFORMAT, *LPPCMWAVEFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - pcmwaveformat_tag
 - mmeapi/pcmwaveformat_tag
 - PPCMWAVEFORMAT
 - mmeapi/PPCMWAVEFORMAT
 - PCMWAVEFORMAT
 - mmeapi/PCMWAVEFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - PCMWAVEFORMAT
---

# PCMWAVEFORMAT structure


## -description

The <b>PCMWAVEFORMAT</b> structure describes the data format for PCM waveform-audio data. This structure has been superseded by the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

## -struct-fields

### -field wf

A <a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a> structure containing general information about the format of the data.

### -field wBitsPerSample

Number of bits per sample.

## -see-also

<a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a>



<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>



<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>
