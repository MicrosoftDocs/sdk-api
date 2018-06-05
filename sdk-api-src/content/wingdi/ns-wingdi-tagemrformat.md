---
UID: NS:wingdi.tagEMRFORMAT
title: tagEMRFORMAT
author: windows-sdk-content
description: The EMRFORMAT structure contains information that identifies graphics data in an enhanced metafile. A GDICOMMENT_MULTIFORMATS enhanced metafile public comment contains an array of EMRFORMAT structures.
old-location: gdi\emrformat.htm
old-project: gdi
ms.assetid: a86e45f1-bbe1-4cb6-a9fa-679108db89ac
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PEMRFORMAT, EMRFORMAT, EMRFORMAT structure [Windows GDI], _win32_EMRFORMAT_str, gdi.emrformat, tagEMRFORMAT, wingdi/EMRFORMAT"
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
tech.root: 
req.typenames: EMRFORMAT, *PEMRFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRFORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRFORMAT structure


## -description



The <b>EMRFORMAT</b> structure contains information that identifies graphics data in an enhanced metafile. A GDICOMMENT_MULTIFORMATS enhanced metafile public comment contains an array of <b>EMRFORMAT</b> structures.




## -struct-fields




### -field dSignature

Contains a picture format identifier. The following identifier values are defined.

<table>
<tr>
<th>Identifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>ENHMETA_SIGNATURE</td>
<td>The picture is in enhanced metafile format.</td>
</tr>
<tr>
<td>EPS_SIGNATURE</td>
<td>The picture is in encapsulated PostScript file format.</td>
</tr>
</table>
 


### -field nVersion

Contains a picture version number. The following version number value is defined.

<table>
<tr>
<th>Version</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>This is the version number of a level 1 encapsulated PostScript file.</td>
</tr>
</table>
 


### -field cbData

The size, in bytes, of the picture data.


### -field offData

Specifies an offset to the picture data. The offset is figured from the start of the GDICOMMENT_MULTIFORMATS public comment within which this <b>EMRFORMAT</b> structure is embedded. The offset must be a <b>DWORD</b> offset.


## -remarks



The reference page for <a href="https://msdn.microsoft.com/80ed11fc-89f8-47ab-8b3b-c817733bd385">GdiComment</a> discusses enhanced metafile public comments in general, and the GDICOMMENT_MULTIFORMATS public comment in particular.




## -see-also




<a href="https://msdn.microsoft.com/80ed11fc-89f8-47ab-8b3b-c817733bd385">GdiComment</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

