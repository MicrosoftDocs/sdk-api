---
UID: NS:winddi._TYPE1_FONT
title: "_TYPE1_FONT"
author: windows-sdk-content
description: The TYPE1_FONT structure contains the information necessary for a PostScript driver to access a Type1 font through GDI.
old-location: display\type1_font.htm
old-project: display
ms.assetid: c852a814-3ebc-4688-aa42-c99b0ee63918
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: TYPE1_FONT, TYPE1_FONT structure [Display Devices], _TYPE1_FONT, display.type1_font, grstrcts_5408143c-ae92-4fa6-b5a8-3ef75b46c30d.xml, winddi/TYPE1_FONT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
tech.root: 
req.typenames: TYPE1_FONT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - TYPE1_FONT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _TYPE1_FONT structure


## -description


The TYPE1_FONT structure contains the information necessary for a PostScript driver to access a Type1 font through GDI.


## -struct-fields




### -field hPFM

Handle to the PostScript Type1 .<a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pfm</a> file.


### -field hPFB

Handle to the PostScript Type1 .<i>pfb</i> file.


### -field ulIdentifier

Is an identifier that is generated and used by GDI. The driver stores <b>ulIdentifier</b> in the <b>dpCharSets</b> field of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure.


## -remarks



A PostScript driver can obtain a list of installed Type1 fonts by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564956">EngGetType1FontList</a>.

Each PostScript Type1 font comes with two separate files: a .<i>pfm</i> file and a .<i>pfb</i> file. The .<i>pfm</i> file contains font metrics information; the .<i>pfb</i> file contains the PostScript Type1 binary font data.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>
 

 

