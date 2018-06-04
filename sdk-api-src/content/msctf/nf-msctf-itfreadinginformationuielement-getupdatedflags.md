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

# ITfReadingInformationUIElement::GetUpdatedFlags


## -description


This method returns the flag that tells which part of this element was updated.


## -parameters




### -param pdwFlags [out]

[out] A pointer to receive the flags that is a combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_CONTEXT"></a><a id="tf_riuie_context"></a><dl>
<dt><b>TF_RIUIE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The target <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_STRING"></a><a id="tf_riuie_string"></a><dl>
<dt><b>TF_RIUIE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_MAXREADINGSTRINGLENGTH"></a><a id="tf_riuie_maxreadingstringlength"></a><dl>
<dt><b>TF_RIUIE_MAXREADINGSTRINGLENGTH</b></dt>
</dl>
</td>
<td width="60%">
The max length of the reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_ERRORINDEX"></a><a id="tf_riuie_errorindex"></a><dl>
<dt><b>TF_RIUIE_ERRORINDEX</b></dt>
</dl>
</td>
<td width="60%">
The error index of the reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_VERTICALORDER"></a><a id="tf_riuie_verticalorder"></a><dl>
<dt><b>TF_RIUIE_VERTICALORDER</b></dt>
</dl>
</td>
<td width="60%">
The vertical order preference was changed.

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
 



