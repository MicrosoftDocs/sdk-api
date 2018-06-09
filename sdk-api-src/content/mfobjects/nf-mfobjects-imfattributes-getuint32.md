---
UID: NF:mfobjects.IMFAttributes.GetUINT32
title: IMFAttributes::GetUINT32
author: windows-sdk-content
description: Retrieves a UINT32 value associated with a key.
old-location: mf\imfattributes_getuint32.htm
old-project: medfound
ms.assetid: e47495e0-3274-4ce2-9fd3-d2fb2afb7578
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetUINT32, GetUINT32 method [Media Foundation], GetUINT32 method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetUINT32 method, IMFAttributes.GetUINT32, IMFAttributes::GetUINT32, e47495e0-3274-4ce2-9fd3-d2fb2afb7578, mf.imfattributes_getuint32, mfobjects/IMFAttributes::GetUINT32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.GetUINT32
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::GetUINT32


## -description



Retrieves a <b>UINT32</b> value associated with a key.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT32</b>.


### -param punValue [out]

Receives a <b>UINT32</b> value. If the key is found and the data type is <b>UINT32</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.


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
The attribute value is not a <b>UINT32</b>.

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



<a href="https://msdn.microsoft.com/b79f3b2c-6293-41b2-afe7-4a0b2c27b34f">MFGetAttributeUINT32</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 

