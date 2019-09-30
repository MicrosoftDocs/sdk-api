---
UID: NS:wingdi.tagEMREXTCREATEPEN
title: EMREXTCREATEPEN (wingdi.h)
author: windows-sdk-content
description: The EMREXTCREATEPEN structure contains members for the ExtCreatePen enhanced metafile record. If the record contains a BITMAPINFO structure, it is followed by the bitmap bits that form a packed device-independent bitmap (DIB).
old-location: gdi\emrextcreatepen.htm
tech.root: gdi
ms.assetid: 9ed97d34-8c03-4b14-821c-397c21c36db0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMREXTCREATEPEN, EMREXTCREATEPEN, EMREXTCREATEPEN structure [Windows GDI], PEMREXTCREATEPEN, PEMREXTCREATEPEN structure pointer [Windows GDI], _win32_EMREXTCREATEPEN_str, gdi.emrextcreatepen, wingdi/EMREXTCREATEPEN, wingdi/PEMREXTCREATEPEN"
ms.topic: struct
f1_keywords: 
 - "wingdi/EMREXTCREATEPEN"
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
 - EMREXTCREATEPEN
targetos: Windows
req.typenames: EMREXTCREATEPEN, *PEMREXTCREATEPEN
req.redist: 
ms.custom: 19H1
---

# EMREXTCREATEPEN structure


## -description



The <b>EMREXTCREATEPEN</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a> enhanced metafile record. If the record contains a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, it is followed by the bitmap bits that form a packed device-independent bitmap (DIB).




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPen

Index to pen in handle table.


### -field offBmi

Offset to <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, if any.


### -field cbBmi

Size of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure, if any.


### -field offBits

Offset to brush bitmap bits, if any.


### -field cbBits

Size of brush bitmap bits, if any.


### -field elp

Extended logical pen, including the <b>elpStyleEntry</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-extlogpen">EXTLOGPEN</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-extlogpen">EXTLOGPEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>
 

 

