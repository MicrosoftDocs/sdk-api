---
UID: NS:wingdi.tagEMREXTSELECTCLIPRGN
title: tagEMREXTSELECTCLIPRGN
author: windows-sdk-content
description: The EMREXTSELECTCLIPRGN structure contains members for the ExtSelectClipRgn enhanced metafile record.
old-location: gdi\emrextselectcliprgn.htm
tech.root: gdi
ms.assetid: fcfa0ae1-06e0-4313-9140-496aa4eec9da
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PEMREXTSELECTCLIPRGN, EMREXTSELECTCLIPRGN, EMREXTSELECTCLIPRGN structure [Windows GDI], PEMREXTSELECTCLIPRGN, PEMREXTSELECTCLIPRGN structure pointer [Windows GDI], _win32_EMREXTSELECTCLIPRGN_str, gdi.emrextselectcliprgn, tagEMREXTSELECTCLIPRGN, wingdi/EMREXTSELECTCLIPRGN, wingdi/PEMREXTSELECTCLIPRGN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
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
 - Wingdi.h
api_name:
 - EMREXTSELECTCLIPRGN
product: Windows
targetos: Windows
req.typenames: EMREXTSELECTCLIPRGN, *PEMREXTSELECTCLIPRGN
req.redist: 
---

# tagEMREXTSELECTCLIPRGN structure


## -description



The <b>EMREXTSELECTCLIPRGN</b> structure contains members for the <a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field cbRgnData

Size of region data, in bytes.


### -field iMode

Operation to be performed. This member must be one of the following values: RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, or RGN_XOR.


### -field RgnData

Buffer containing a <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

