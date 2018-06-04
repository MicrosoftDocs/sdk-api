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

# DPA_LoadStream function


## -description


<p class="CCE_Message">[<b>DPA_LoadStream</b> is available in Windows Vista. It might be altered or unavailable in subsequent versions. ]

Loads the dynamic pointer array (DPA) from a stream by calling the specified callback function to read each element.


## -parameters




### -param phdpa

TBD


### -param pfn [in]

Type: <b><a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a></b>

The callback function. See <a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a> for the callback function prototype. 


### -param pstream

TBD


### -param pvInstData [in]

Type: <b>void*</b>

A pointer to callback data. <i>pvInstData</i> is passed as a parameter to <i>pfn</i>. 


#### - ppdpa [out]

Type: <b>HDPA*</b>

A handle to a DPA.


#### - pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the following values.

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
Indicates that the callback function was successful and the element was loaded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the callback function was unsuccessful in loading the element; however, the process should continue. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that one or more of the parameters is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the stream object could not be read. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The buffer length is invalid or there was insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



This function must be called directly from ComCtl32.dll. It is ordinal 9.

The callback is responsible for writing the <i>pvInstData</i> data to the stream.



