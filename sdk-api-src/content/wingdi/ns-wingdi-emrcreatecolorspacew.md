---
UID: NS:wingdi.tagEMRCREATECOLORSPACEW
title: EMRCREATECOLORSPACEW (wingdi.h)
author: windows-sdk-content
description: The EMRCREATECOLORSPACEW structure contains members for the CreateColorSpace enhanced metafile record. It differs from EMRCREATECOLORSPACE in that it has a Unicode logical color space and also has an optional array containing raw source profile data.
old-location: gdi\emrcreatecolorspacew.htm
tech.root: gdi
ms.assetid: eac364ad-ef17-4f60-ac4c-39d8a9af618b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRCREATECOLORSPACEW, EMRCREATECOLORSPACEW, EMRCREATECOLORSPACEW structure [Windows GDI], PEMRCREATECOLORSPACEW, PEMRCREATECOLORSPACEW structure pointer [Windows GDI], _win32_EMRCREATECOLORSPACEW_str, gdi.emrcreatecolorspacew, wingdi/EMRCREATECOLORSPACEW, wingdi/PEMRCREATECOLORSPACEW"
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
 - EMRCREATECOLORSPACEW
product: Windows
targetos: Windows
req.typenames: EMRCREATECOLORSPACEW, *PEMRCREATECOLORSPACEW
req.redist: 
ms.custom: 19H1
---

# EMRCREATECOLORSPACEW structure


## -description



The <b>EMRCREATECOLORSPACEW</b> structure contains members for the <a href="https://msdn.microsoft.com/c3fc798c-4bb9-4010-87d4-edc0005b7698">CreateColorSpace</a> enhanced metafile record. 
		  It differs from <a href="https://msdn.microsoft.com/ee2e02bb-5bd2-460c-aefe-78a143c72ff6">EMRCREATECOLORSPACE</a> in that it has a Unicode logical color space and also has an optional array containing raw source profile data.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihCS

Index of the color space in handle table.


### -field lcs

Logical color space. Note, this is the Unicode version of the structure.


### -field dwFlags

Can be the following.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>CREATECOLORSPACE_EMBEDED</td>
<td>Indicates that a color space is embedded in the metafile.</td>
</tr>
</table>
 


### -field cbData

Size of the raw source profile data in bytes, if it is attached.


### -field Data

An array containing the source profile data. The size of the array is <b>cbData</b>.


## -see-also




<a href="https://msdn.microsoft.com/c3fc798c-4bb9-4010-87d4-edc0005b7698">CreateColorSpace</a>



<a href="https://msdn.microsoft.com/ee2e02bb-5bd2-460c-aefe-78a143c72ff6">EMRCREATECOLORSPACE</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

