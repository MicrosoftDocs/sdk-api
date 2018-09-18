---
UID: NF:mfobjects.IMFAttributes.GetAllocatedBlob
title: IMFAttributes::GetAllocatedBlob
author: windows-sdk-content
description: Retrieves a byte array associated with a key. This method allocates the memory for the array.
old-location: mf\imfattributes_getallocatedblob.htm
tech.root: medfound
ms.assetid: 380e0e3a-b5c5-4d31-8793-417262377fef
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 380e0e3a-b5c5-4d31-8793-417262377fef, GetAllocatedBlob, GetAllocatedBlob method [Media Foundation], GetAllocatedBlob method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetAllocatedBlob method, IMFAttributes.GetAllocatedBlob, IMFAttributes::GetAllocatedBlob, mf.imfattributes_getallocatedblob, mfobjects/IMFAttributes::GetAllocatedBlob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFAttributes.GetAllocatedBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::GetAllocatedBlob


## -description



Retrieves a byte array associated with a key. This method allocates the memory for the array.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_BLOB</b>.


### -param ppBuf [out]

If the key is found and the value is a byte array, this parameter receives a copy of the array. The caller must free the memory for the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcbSize [out]

Receives the size of the array, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a byte array.

</td>
</tr>
</table>
 




## -remarks



To copy a byte array value into a caller-allocated buffer, use the <a href="https://msdn.microsoft.com/68528db7-90df-4abe-a957-ffb8c3f12cef">IMFAttributes::GetBlob</a> method.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 

