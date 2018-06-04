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

# tagCOLORMATCHTOTARGET structure


## -description



The <b>EMRCOLORMATCHTOTARGET</b> structure contains members for the <a href="https://msdn.microsoft.com/eb922411-0808-4404-bdaf-bf29d0cad379">ColorMatchToTarget</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field dwAction

The action to be taken. This member can be one of the following values.

<table>
<tr>
<th>Action</th>
<th>Meaning</th>
</tr>
<tr>
<td>CS_ENABLE</td>
<td>Maps colors to the target device's color gamut. This enables color proofing. All subsequent draw commands to the DC will render colors as they would appear on the target device.</td>
</tr>
<tr>
<td>CS_DISABLE</td>
<td>Disables color proofing.</td>
</tr>
<tr>
<td>CS_DELETE_TRANSFORM</td>
<td>If color management is enabled for the target profile, disables it and deletes the concatenated transform.</td>
</tr>
</table>
 


### -field dwFlags

This parameter can be the following value.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>COLORMATCHTOTARGET_EMBEDED</td>
<td>Indicates that a color profile has been embedded in the metafile.</td>
</tr>
</table>
 


### -field cbName

The size of the desired target profile name, in bytes.


### -field cbData

The size of the raw target profile data in bytes, if it is attached.


### -field Data

An array containing the target profile name and the raw target profile data. 
			 The size of the array is <b>cbName</b> + <b>cbData</b>. 
			 If <b>cbData</b> is nonzero the raw target profile data is attached and follows the target profile name at location <b>Data</b>[<b>cbName</b>].


## -see-also




<a href="https://msdn.microsoft.com/eb922411-0808-4404-bdaf-bf29d0cad379">ColorMatchToTarget</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

