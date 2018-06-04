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

# ITextStoreAnchor::GetSelection


## -description


The <b>ITextStoreAnchor::GetSelection</b> method returns the offset of a text selection in a text stream. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.


## -parameters




### -param ulIndex [in]

Specifies the text selections that start the process. If the <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_DEFAULT_SELECTION</a> constant is specified for this parameter, the input selection starts the process, and only a single selection (the one appropriate for input operations) will be returned.


### -param ulCount [in]

Specifies the maximum number of selections to return.


### -param pSelection [out]

Receives the style, start, and end character positions of the selected text. These values are put into the <a href="https://msdn.microsoft.com/56fbe145-1972-4b44-a730-17860e428dd0">TS_SELECTION_ANCHOR</a> structure.


### -param pcFetched [out]

Receives the number of <i>pSelection</i> structures returned.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to load the start or end anchor into the <b>TS_SELECTION_ANCHOR</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf8bbe66-d2ad-49b3-9e7c-246e4ca50149">Edit Contexts</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">
        ITextStoreAnchor::SetSelection
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



TF_DEFAULT_SELECTION



<a href="https://msdn.microsoft.com/56fbe145-1972-4b44-a730-17860e428dd0">TS_SELECTION_ANCHOR
      </a>
 

 

