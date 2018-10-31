---
UID: NF:d2d1_1.ID2D1Properties.SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE,UINT32)
title: ID2D1Properties::SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE,UINT32)
author: windows-sdk-content
description: Sets the named property to the given value.
old-location: direct2d\id2d1properties_setvaluebyname__pcwstr__d2d1_property_type__const_byte__datasize_.htm
tech.root: direct2d
ms.assetid: 53C31C95-4273-4588-A264-90A431DAE3DE
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ID2D1Properties interface [Direct2D],SetValueByName method, ID2D1Properties.SetValueByName, ID2D1Properties.SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE,UINT32), ID2D1Properties::SetValueByName, ID2D1Properties::SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE*,UINT32), ID2D1Properties::SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE,UINT32), SetValueByName, SetValueByName method [Direct2D], SetValueByName method [Direct2D],ID2D1Properties interface, d2d1_1/ID2D1Properties::SetValueByName, direct2d.id2d1properties_setvaluebyname__pcwstr__d2d1_property_type__const_byte__datasize_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.SetValueByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,const BYTE,UINT32)


## -description


Sets the named property to the given value.  


## -parameters




### -param name [in]

The name of the property to set.


### -param type

The type of the property to set.


### -param data [in]

The data to set.


### -param dataSize

The number of bytes in the data to set.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_INVALID_PROPERTY</td>
<td>The specified property does not exist.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Failed to allocate necessary memory.</td>
</tr>
<tr>
<td>D3DERR_OUT_OF_VIDEO_MEMORY</td>
<td>Failed to allocate required video memory.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>Unspecified failure.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

