---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

