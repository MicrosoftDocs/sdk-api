---
UID: NS:wingdi.tagEMREXTCREATEPEN
title: tagEMREXTCREATEPEN
author: windows-sdk-content
description: The EMREXTCREATEPEN structure contains members for the ExtCreatePen enhanced metafile record. If the record contains a BITMAPINFO structure, it is followed by the bitmap bits that form a packed device-independent bitmap (DIB).
old-location: gdi\emrextcreatepen.htm
tech.root: gdi
ms.assetid: 9ed97d34-8c03-4b14-821c-397c21c36db0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PEMREXTCREATEPEN, EMREXTCREATEPEN, EMREXTCREATEPEN structure [Windows GDI], PEMREXTCREATEPEN, PEMREXTCREATEPEN structure pointer [Windows GDI], _win32_EMREXTCREATEPEN_str, gdi.emrextcreatepen, tagEMREXTCREATEPEN, wingdi/EMREXTCREATEPEN, wingdi/PEMREXTCREATEPEN"
ms.prod: windows
ms.technology: windows-sdk
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
 - EMREXTCREATEPEN
product: Windows
targetos: Windows
req.typenames: EMREXTCREATEPEN, *PEMREXTCREATEPEN
req.redist: 
---

# tagEMREXTCREATEPEN structure


## -description



The <b>EMREXTCREATEPEN</b> structure contains members for the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> enhanced metafile record. If the record contains a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, it is followed by the bitmap bits that form a packed device-independent bitmap (DIB).




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPen

Index to pen in handle table.


### -field offBmi

Offset to <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, if any.


### -field cbBmi

Size of <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, if any.


### -field offBits

Offset to brush bitmap bits, if any.


### -field cbBits

Size of brush bitmap bits, if any.


### -field elp

Extended logical pen, including the <b>elpStyleEntry</b> member of the <a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

