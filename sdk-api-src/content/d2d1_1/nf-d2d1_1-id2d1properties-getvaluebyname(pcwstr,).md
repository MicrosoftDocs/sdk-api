---
UID: NF:d2d1_1.ID2D1Properties.GetValueByName(PCWSTR,)
title: ID2D1Properties::GetValueByName(PCWSTR,)
author: windows-sdk-content
description: Gets the property value by name.
old-location: direct2d\id2d1properties_getvaluebyname.htm
tech.root: direct2d
ms.assetid: 2dc60fad-9ce2-4951-85ea-647a828420a1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetValueByName, GetValueByName method [Direct2D], GetValueByName method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValueByName method, ID2D1Properties.GetValueByName, ID2D1Properties.GetValueByName(PCWSTR,), ID2D1Properties::GetValueByName, ID2D1Properties::GetValueByName(PCWSTR,), ID2D1Properties::GetValueByName(PCWSTR,BYTE*,UINT32), d2d1_1/ID2D1Properties::GetValueByName, direct2d.id2d1properties_getvaluebyname
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
 - ID2D1Properties.GetValueByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Properties::GetValueByName(PCWSTR,)


## -description


Gets the property value by name.


## -parameters




### -param propertyName

TBD


### -param arg1

TBD




#### - data [out]

Type: <b>BYTE*</b>

When this method returns, contains the buffer with  the data value.


#### - dataSize

Type: <b>UINT32</b>

The number of bytes in the data to be retrieved.


#### - name [in]

Type: <b>PCWSTR</b>

The property name to get.


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
 




## -remarks



If <i>name</i> does not exist, no information is retrieved.

Any error not in the standard set returned by a property implementation will be mapped into the standard error range.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>
 

 

