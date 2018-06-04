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

# IWiaDataTransfer::idtEnumWIA_FORMAT_INFO


## -description


The <b>IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</b> method creates a banded transfer implementation of the <a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a> interface.


## -parameters




### -param ppEnum [out]

Type: <b><a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a> interface.


## -returns



Type: <b>HRESULT</b>

If it fails for any reason other than those specified in the following table, this method will return a standard COM error.

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The <i>ppEnum</i> parameter is not the address of a pointer to the <a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a> interface.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is not enough memory to create the enumerator object.</td>
</tr>
<tr>
<td>S_OK</td>
<td>The enumerator object was successfully created.</td>
</tr>
</table>
 




## -remarks



This method creates the <a href="https://msdn.microsoft.com/9f3e94bc-fa90-4e3d-97c5-17e57055de0e">IEnumWIA_FORMAT_INFO</a> interface that applications use to enumerate an array of <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structures. This provides applications with the ability to determine the formats and media types of incoming data when transferring banded data.

Note that applications must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppEnum</i> parameter.



