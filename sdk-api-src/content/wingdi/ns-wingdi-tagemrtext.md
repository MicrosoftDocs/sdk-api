---
UID: NS:wingdi.tagEMRTEXT
title: tagEMRTEXT
author: windows-sdk-content
description: The EMRTEXT structure contains members for text output.
old-location: gdi\emrtext.htm
tech.root: gdi
ms.assetid: a126f1ea-35ef-492d-8184-fb288a74f7f6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PEMRTEXT, EMRTEXT, EMRTEXT structure [Windows GDI], PEMRTEXT, PEMRTEXT structure pointer [Windows GDI], _win32_EMRTEXT_str, gdi.emrtext, tagEMRTEXT, wingdi/EMRTEXT, wingdi/PEMRTEXT"
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
 - EMRTEXT
product: Windows
targetos: Windows
req.typenames: EMRTEXT, *PEMRTEXT
req.redist: 
---

# tagEMRTEXT structure


## -description



The <b>EMRTEXT</b> structure contains members for text output.




## -struct-fields




### -field ptlReference

The logical coordinates of the reference point used to position the string.


### -field nChars

The number of characters in the string.


### -field offString

The offset to the string.


### -field fOptions

A value that indicates how to use the application-defined rectangle. This member can be a combination of the ETO_CLIPPED and ETO_OPAQUE values.


### -field rcl

An optional clipping and/or opaquing rectangle, in logical units.


### -field offDx

The offset to the intercharacter spacing array.


## -remarks



The <b>EMRTEXT</b> structure is used as a member in the <a href="https://msdn.microsoft.com/1d9b0b32-6a51-481a-9589-3de832d746d7">EMREXTTEXTOUT</a> and <a href="https://msdn.microsoft.com/9c1decdd-fe6f-4220-abba-7547ab5427ba">EMRPOLYTEXTOUT</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a>



<a href="https://msdn.microsoft.com/47a89d2d-4733-47be-91c1-450845e78075">RECTL</a>
 

 

