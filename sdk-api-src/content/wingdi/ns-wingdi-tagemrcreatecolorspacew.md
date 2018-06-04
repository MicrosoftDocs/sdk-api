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

# tagEMRCREATECOLORSPACEW structure


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
 

 

