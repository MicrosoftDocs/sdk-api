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

# PropVariantToVariant function


## -description


Converts the contents of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -parameters




### -param pPropVar [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pVar [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure. When this function returns, the <b>VARIANT</b> contains the converted information.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Normally, the data stored in the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is copied to the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> without a datatype change. However, in the following cases, there is no direct <b>VARIANT</b> support for the datatype, and they are converted as shown.
                
                


<table class="clsStd">
<tr>
<th>Original <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> Type</th>
<th>Stored as <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> Type</th>
</tr>
<tr>
<td>VT_BLOB, VT_STREAM</td>
<td>VT_UNKNOWN. The <b>punkVal</b> member will contain a pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that contains the source data.</td>
</tr>
<tr>
<td>VT_LPSTR, VT_LPWSTR, VT_CLSID</td>
<td>VT_BSTR</td>
</tr>
<tr>
<td>VT_FILETIME</td>
<td>VT_DATE</td>
</tr>
<tr>
<td>VT_VECTOR|x</td>
<td>VT_ARRAY|y</td>
</tr>
</table>
 



The following types cannot be converted with this function.
            
                

<ul>
<li>VT_STORAGE</li>
<li>VT_BLOB_OBJECT</li>
<li>VT_STREAMED_OBJECT</li>
<li>VT_STORED_OBJECT</li>
<li>VT_CF</li>
<li>VT_VECTOR | VT_CF</li>
</ul>


