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

# IFont::get_hFont


## -description


Retrieves a handle to the font described by this font object.


## -parameters




### -param phFont [out]

A pointer to the caller-allocated variable that receives the font handle. 
      The caller does not own this resource and must not attempt to destroy the font.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_OUTOFMEMORY</b>, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The font handle was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>phFont</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The font object maintains ownership of the <b>HFONT</b> and can destroy it 
    at any time without prior notification. If the caller needs to secure this font for a limited period of time, it 
    can call <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a> and 
    <a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">IFont::ReleaseHfont</a>.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">IFont::AddRefHfont</a>



<a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">IFont::ReleaseHfont</a>
 

 

