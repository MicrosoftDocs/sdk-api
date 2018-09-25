---
UID: NF:d2d1_1.ID2D1Properties.GetValue(UINT32,BYTE,UINT32)
title: ID2D1Properties::GetValue(UINT32,BYTE,UINT32)
author: windows-sdk-content
description: Gets the value of the specified property by index.
old-location: direct2d\id2d1properties_getvalue.htm
tech.root: direct2d
ms.assetid: 01678e13-df23-47bb-9af7-9f2ecaf03577
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetValue, GetValue method [Direct2D], GetValue method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValue method, ID2D1Properties.GetValue, ID2D1Properties.GetValue(UINT32,BYTE,UINT32), ID2D1Properties::GetValue, ID2D1Properties::GetValue(UINT32,BYTE*,UINT32), ID2D1Properties::GetValue(UINT32,BYTE,UINT32), d2d1_1/ID2D1Properties::GetValue, direct2d.id2d1properties_getvalue
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
 - ID2D1Properties.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetValue(UINT32,BYTE,UINT32)


## -description


Gets  the value of the specified property by index.


## -parameters




### -param index

Type: <b>UINT32</b>

The index of the property from which the data is to be obtained.


#### - data [out]

Type: <b>BYTE*</b>

When this method returns, contains a pointer to the data requested.


#### - dataSize

Type: <b>UINT32</b>

The number of bytes in the data to be retrieved.


## -returns



Type: <b>HRESULT</b>

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




<a href="https://msdn.microsoft.com/7261ea3c-bd52-4809-93c8-9e7a0a7424d0">D2D1_PROPERTY</a>



<a href="https://msdn.microsoft.com/311a1b6f-ef0e-4453-a5fe-d06ebb0bb222">D2D1_SUBPROPERTY</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

