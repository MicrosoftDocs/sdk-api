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

# PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN callback function


## -description


Called by the Windows Biometric Framework to determine the capabilities and limitations of the biometric storage component.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param StorageInfo [out]

Pointer to the <a href="https://msdn.microsoft.com/7A648610-E947-4967-A9AF-C8A9C0B81D92">WINBIO_EXTENDED_STORAGE_INFO</a> structure that contains the storage information returned by this function.


### -param StorageInfoSize [in]

The specified size of the storage information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

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
The <i>Pipeline</i> and <i>StorageInfo</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>StorageInfoSize</i> value is less than the size needed to return the storage information.

</td>
</tr>
</table>
 




## -remarks



This method is called once during configuration of the biometric unit. 

It will also be called if a client application uses the <a href="https://msdn.microsoft.com/63e38e74-3d46-4474-a31c-eaf724156bc6">WinBioGetProperty</a> function to query the value of the <b>WINBIO_PROPERTY_EXTENDED_STORAGE_INFO</b> property.



