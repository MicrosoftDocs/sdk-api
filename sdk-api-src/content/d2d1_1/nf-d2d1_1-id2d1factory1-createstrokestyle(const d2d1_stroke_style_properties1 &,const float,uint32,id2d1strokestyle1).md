---
UID: NF:d2d1_1.ID2D1Factory1.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1)
title: ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1)
author: windows-sdk-content
description: Creates a ID2D1StrokeStyle1 object.
old-location: direct2d\id2d1factory1_createstrokestyle2.htm
tech.root: direct2d
ms.assetid: 4DEB9CDE-ABE2-47CB-BB06-27535F89D793
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateStrokeStyle, CreateStrokeStyle method [Direct2D], CreateStrokeStyle method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateStrokeStyle method, ID2D1Factory1.CreateStrokeStyle, ID2D1Factory1.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1), ID2D1Factory1::CreateStrokeStyle, ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1), d2d1_1/ID2D1Factory1::CreateStrokeStyle, direct2d.id2d1factory1_createstrokestyle2
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
 - ID2D1Factory1.CreateStrokeStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1)


## -description


Creates a <a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a> object.


## -parameters




### -param strokeStyleProperties [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/6bed0f23-be10-4265-8edd-ccf82ce0e683">D2D1_STROKE_STYLE_PROPERTIES1</a></b>

The stroke style properties to apply.


### -param dashes [in]

Type: <b>const <a href="https://msdn.microsoft.com/540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0">FLOAT</a>*</b>

An array of widths for the dashes and gaps.


### -param dashesCount

Type: <b><a href="https://msdn.microsoft.com/62a8da3a-3e5d-4ce8-bda5-08f84255ba3f">UINT</a></b>

The size of the dash array.


### -param strokeStyle [out]

Type: <b>const <a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a>**</b>

When this method returns, contains the address of a pointer to the  newly created stroke style.


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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>
 




## -remarks



It is valid to specify a dash array only if D2D1_DASH_STYLE_CUSTOM is also specified.




## -see-also




<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>



<a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a>
 

 

