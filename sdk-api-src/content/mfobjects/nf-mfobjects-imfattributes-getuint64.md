---
UID: NF:mfobjects.IMFAttributes.GetUINT64
title: IMFAttributes::GetUINT64
author: windows-sdk-content
description: Retrieves a UINT64 value associated with a key.
old-location: mf\imfattributes_getuint64.htm
tech.root: medfound
ms.assetid: f3240fff-48d8-4d88-8c75-15f00bfe72ed
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetUINT64, GetUINT64 method [Media Foundation], GetUINT64 method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetUINT64 method, IMFAttributes.GetUINT64, IMFAttributes::GetUINT64, f3240fff-48d8-4d88-8c75-15f00bfe72ed, mf.imfattributes_getuint64, mfobjects/IMFAttributes::GetUINT64
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
 - IMFAttributes.GetUINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::GetUINT64


## -description



Retrieves a <b>UINT64</b> value associated with a key.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT64</b>.


### -param punValue [out]

Receives a <b>UINT64</b> value. If the key is found and the data type is <b>UINT64</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.


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
The attribute value is not a <b>UINT64</b>.
              

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/843946a4-d270-4440-9818-59e95cbf9a5b">MFGetAttributeUINT64</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 

