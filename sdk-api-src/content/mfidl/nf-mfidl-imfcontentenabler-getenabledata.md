---
UID: NF:mfidl.IMFContentEnabler.GetEnableData
title: IMFContentEnabler::GetEnableData
author: windows-sdk-content
description: Retrieves the data for a manual content enabling action.
old-location: mf\imfcontentenabler_getenabledata.htm
tech.root: medfound
ms.assetid: d1859037-7a33-4943-8ca9-6782fc8b0b92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnableData, GetEnableData method [Media Foundation], GetEnableData method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],GetEnableData method, IMFContentEnabler.GetEnableData, IMFContentEnabler::GetEnableData, d1859037-7a33-4943-8ca9-6782fc8b0b92, mf.imfcontentenabler_getenabledata, mfidl/IMFContentEnabler::GetEnableData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentEnabler.GetEnableData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentEnabler::GetEnableData


## -description



Retrieves the data for a manual content enabling action.




## -parameters




### -param ppbData [out]

Receives a pointer to a buffer that contains the data. The caller must free the buffer by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcbData [out]

Receives the size of the <i>ppbData</i> buffer.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No data is available.

</td>
</tr>
</table>
 




## -remarks



The purpose of the data depends on the content enabler type, which is obtained by calling <a href="https://msdn.microsoft.com/9fe597d8-788c-48c4-a21a-0b91a890710f">IMFContentEnabler::GetEnableType</a>.

<table>
<tr>
<th>Enable type</th>
<th>Purpose of data</th>
</tr>
<tr>
<td>Individualization</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>License acquisition</td>
<td>HTTP POST data.</td>
</tr>
<tr>
<td>Revocation</td>
<td>
<a href="https://msdn.microsoft.com/df12e64b-92e3-4446-bade-3ad55cbedf51">MFRR_COMPONENTS</a> structure.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/85d98f49-8af2-42ce-9b36-a025aee93f73">How to Play Protected Media Files</a>



<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a>
 

 

