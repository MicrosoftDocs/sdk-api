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

# _IMAGEHLP_CBA_EVENT structure


## -description


Contains information about a debugging event.


## -struct-fields




### -field severity

The event severity. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="sevInfo"></a><a id="sevinfo"></a><a id="SEVINFO"></a><dl>
<dt><b>sevInfo</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Informational event.

</td>
</tr>
<tr>
<td width="40%"><a id="sevProblem"></a><a id="sevproblem"></a><a id="SEVPROBLEM"></a><dl>
<dt><b>sevProblem</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="sevAttn"></a><a id="sevattn"></a><a id="SEVATTN"></a><dl>
<dt><b>sevAttn</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="sevFatal"></a><a id="sevfatal"></a><a id="SEVFATAL"></a><dl>
<dt><b>sevFatal</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>
 


### -field code

This member is reserved for future use.


### -field desc

A text description of the error.


### -field object

This member is reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/f3ba952b-ecc5-4235-a806-00c82d40e611">SymRegisterCallbackProc64</a>



<a href="https://msdn.microsoft.com/11c833ee-a9f3-4d08-a6cd-0da62844c589">SymbolServerCallback</a>
 

 

