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

# ITfCandidateListUIElement::GetUpdatedFlags


## -description


The <b>ITfCandidateListUIElement::GetUpdatedFlags</b> method returns the flag that tells which part of this element was updated.


## -parameters




### -param pdwFlags [out]

[out] a pointer to receive the flags that is a combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_DOCUMENTMGR"></a><a id="tf_cluie_documentmgr"></a><dl>
<dt><b>TF_CLUIE_DOCUMENTMGR</b></dt>
</dl>
</td>
<td width="60%">
The target document manager was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_COUNT"></a><a id="tf_cluie_count"></a><dl>
<dt><b>TF_CLUIE_COUNT</b></dt>
</dl>
</td>
<td width="60%">
The count of the candidate string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_SELECTION"></a><a id="tf_cluie_selection"></a><dl>
<dt><b>TF_CLUIE_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
The selection of the candidate was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_STRING"></a><a id="tf_cluie_string"></a><dl>
<dt><b>TF_CLUIE_STRING</b></dt>
</dl>
</td>
<td width="60%">
Some strings in the list were changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_PAGEINDEX"></a><a id="tf_cluie_pageindex"></a><dl>
<dt><b>TF_CLUIE_PAGEINDEX</b></dt>
</dl>
</td>
<td width="60%">
The current page index or some page index was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_CURRENTPAGE"></a><a id="tf_cluie_currentpage"></a><dl>
<dt><b>TF_CLUIE_CURRENTPAGE</b></dt>
</dl>
</td>
<td width="60%">
The page was changed.

</td>
</tr>
</table>
 


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
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



