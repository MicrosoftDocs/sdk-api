---
UID: NS:wingdi._PSFEATURE_CUSTPAPER
title: "_PSFEATURE_CUSTPAPER"
author: windows-sdk-content
description: The PSFEATURE_CUSTPAPER structure contains information about a custom paper size for a PostScript driver. This structure is used with the GET_PS_FEATURESETTING printer escape function.
old-location: gdi\psfeature_custpaper.htm
tech.root: printdocs
ms.assetid: 3858154c-425f-4333-a637-6d977caf7290
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "*PPSFEATURE_CUSTPAPER, PPSFEATURE_CUSTPAPER, PPSFEATURE_CUSTPAPER structure pointer [Windows GDI], PSFEATURE_CUSTPAPER, PSFEATURE_CUSTPAPER structure [Windows GDI], _PSFEATURE_CUSTPAPER, _win32_PSFEATURE_CUSTPAPER_str, gdi.psfeature_custpaper, wingdi/PPSFEATURE_CUSTPAPER, wingdi/PSFEATURE_CUSTPAPER"
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
 - PSFEATURE_CUSTPAPER
product: Windows
targetos: Windows
req.typenames: PSFEATURE_CUSTPAPER, *PPSFEATURE_CUSTPAPER
req.redist: 
---

# _PSFEATURE_CUSTPAPER structure


## -description



The <b>PSFEATURE_CUSTPAPER</b> structure contains information about a custom paper size for a PostScript driver. This structure is used with the <a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a> printer escape function.




## -struct-fields




### -field lOrientation

Indicates the custom paper orientation. This member can be 0 to 3 if custom page size is selected. Otherwise, it is 1 and all other structure members are zero


### -field lWidth

Custom page width, in points.


### -field lHeight

Custom page height, in points.


### -field lWidthOffset

Custom page width offset, in points.


### -field lHeightOffset

Custom page height offset, in points.


## -remarks



For the semantics of the <b>lOrientation</b>, <b>lWidth</b>, <b>lHeight</b>, <b>lWidthOffset</b>, and <b>lHeightOffset</b> members, please refer to "Custom Page Size Parameters" in "PostScript Printer Description File Format Specification" v.4.3.




## -see-also




<a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

