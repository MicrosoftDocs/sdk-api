---
UID: NS:winddi._TYPE1_FONT
title: TYPE1_FONT (winddi.h)
author: windows-sdk-content
description: The TYPE1_FONT structure contains the information necessary for a PostScript driver to access a Type1 font through GDI.
old-location: display\type1_font.htm
tech.root: display
ms.assetid: c852a814-3ebc-4688-aa42-c99b0ee63918
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TYPE1_FONT, TYPE1_FONT structure [Display Devices], display.type1_font, grstrcts_5408143c-ae92-4fa6-b5a8-3ef75b46c30d.xml, winddi/TYPE1_FONT
ms.topic: struct
f1_keywords: 
 - "winddi/TYPE1_FONT"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: TYPE1_FONT
req.redist: 
ms.custom: 19H1
---

# TYPE1_FONT structure


## -description


The TYPE1_FONT structure contains the information necessary for a PostScript driver to access a Type1 font through GDI.


## -struct-fields




### -field hPFM

Handle to the PostScript Type1 .<a href="https://docs.microsoft.com/windows-hardware/drivers/">pfm</a> file.


### -field hPFB

Handle to the PostScript Type1 .<i>pfb</i> file.


### -field ulIdentifier

Is an identifier that is generated and used by GDI. The driver stores <b>ulIdentifier</b> in the <b>dpCharSets</b> field of the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_ifimetrics">IFIMETRICS</a> structure.


## -remarks



A PostScript driver can obtain a list of installed Type1 fonts by calling <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-enggettype1fontlist">EngGetType1FontList</a>.

Each PostScript Type1 font comes with two separate files: a .<i>pfm</i> file and a .<i>pfb</i> file. The .<i>pfm</i> file contains font metrics information; the .<i>pfb</i> file contains the PostScript Type1 binary font data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_ifimetrics">IFIMETRICS</a>
 

 

