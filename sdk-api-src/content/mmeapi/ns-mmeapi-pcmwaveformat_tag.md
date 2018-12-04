---
UID: NS:mmeapi.pcmwaveformat_tag
title: pcmwaveformat_tag
author: windows-sdk-content
description: The PCMWAVEFORMAT structure describes the data format for PCM waveform-audio data. This structure has been superseded by the WAVEFORMATEX structure.
old-location: multimedia\pcmwaveformat.htm
tech.root: Multimedia
ms.assetid: c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPPCMWAVEFORMAT, *NPPCMWAVEFORMAT, *PPCMWAVEFORMAT, PCMWAVEFORMAT, PCMWAVEFORMAT structure [Windows Multimedia], _win32_PCMWAVEFORMAT_str, mmeapi/PCMWAVEFORMAT, multimedia.pcmwaveformat, pcmwaveformat_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mmeapi.h
req.include-header: Windows.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - PCMWAVEFORMAT
product: Windows
targetos: Windows
req.typenames: PCMWAVEFORMAT, *PPCMWAVEFORMAT, *NPPCMWAVEFORMAT, *LPPCMWAVEFORMAT
req.redist: 
---

# pcmwaveformat_tag structure


## -description



The <b>PCMWAVEFORMAT</b> structure describes the data format for PCM waveform-audio data. This structure has been superseded by the <a href="https://msdn.microsoft.com/bd0f96ec-d26a-4e6f-8802-50e8ff207f54">WAVEFORMATEX</a> structure.




## -struct-fields




### -field wf

A <a href="https://msdn.microsoft.com/48871868-792a-4479-9e92-95306c25673a">WAVEFORMAT</a> structure containing general information about the format of the data.


### -field wBitsPerSample

Number of bits per sample.


## -see-also




<a href="https://msdn.microsoft.com/48871868-792a-4479-9e92-95306c25673a">WAVEFORMAT</a>



<a href="https://msdn.microsoft.com/bd0f96ec-d26a-4e6f-8802-50e8ff207f54">WAVEFORMATEX</a>



<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/4ae84ba8-f444-4d9e-adc8-343b4ee764cc">Waveform Structures</a>
 

 

