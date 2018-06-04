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

# IAudioProcessingObject::Initialize


## -description


The Initialize method initializes the APO and supports data of variable length.


## -parameters




### -param cbDataSize [in]

This is the size, in bytes, of the initialization data.


### -param pbyData [in]

This is initialization data that is specific to this APO.


## -returns



The <code>Initialize</code> method returns a value of S_OK if the call was successful. Otherwise, this method returns one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
APO already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULTS</b></dt>
</dl>
</td>
<td width="60%">
These additional error conditions are tracked by the audio engine.

</td>
</tr>
</table>
 




## -remarks



If this method is used to initialize an APO without the need to initialize any data, it is acceptable to supply a <b>NULL</b> as the value of the pbyData parameter and a 0 (zero) as the value of the cbDataSize parameter. The data that is supplied is of variable length and must have the following format:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Struct MyAPOInitializationData
{
APOInitBaseStruct APOInit;
// list additional struct members here
// ...
};</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj151545">APOInitBaseStruct</a>
 

 

