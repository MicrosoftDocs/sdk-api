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

# IITWordWheel::Open


## -description


Opens a word wheel.




## -parameters




### -param lpITDB [in]

Pointer to <a href="https://msdn.microsoft.com/16051c95-5fad-43ea-9b85-a4754077dc3c">database object</a>.




### -param lpszMoniker [in]

Name of word wheel.




### -param dwFlags [in]

One or more of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ITWW_OPEN_CONNECT"></a><a id="itww_open_connect"></a><dl>
<dt><b>ITWW_OPEN_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  If the word wheel resides on a remote computer, connect to the computer during this call to retrieve initialization data. Otherwise the connection is delayed until the first API call that requires this data.</div>
<div> </div>
</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

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
The word wheel was successfully opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ALREADYOPEN</b></dt>
</dl>
</td>
<td width="60%">
Word wheel is already open.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/16051c95-5fad-43ea-9b85-a4754077dc3c">IITDatabase</a>* interface or <i>lpszMoniker</i> parameter was NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E*</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface errors that can occur as storage is opened.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9734c73e-9325-4a6d-bbf3-3f87f96a662e">IITWordWheel</a>
 

 

