---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateColorContext
title: ID2D1DeviceContext::CreateColorContext
author: windows-sdk-content
description: Creates a color context.
old-location: direct2d\id2d1devicecontext_createcolorcontext.htm
tech.root: direct2d
ms.assetid: 4e03dfe6-b114-46da-820e-341c554b178b
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateColorContext, CreateColorContext method [Direct2D], CreateColorContext method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateColorContext method, ID2D1DeviceContext.CreateColorContext, ID2D1DeviceContext::CreateColorContext, d2d1_1/ID2D1DeviceContext::CreateColorContext, direct2d.id2d1devicecontext_createcolorcontext
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
req.lib: 
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
 - ID2D1DeviceContext.CreateColorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateColorContext


## -description


Creates a color context.


## -parameters




### -param space

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

The space  of color context to create.


### -param profile

TBD


### -param profileSize

Type: <b>UINT32</b>

The size in bytes of <i>Profile</i>.


### -param colorContext [out]

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to a new color context object.


#### - Profile [in, optional]

Type: <b>const BYTE*</b>

A buffer containing the ICC profile bytes used to initialize the color context when <i>space</i> is <a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE_CUSTOM</a>.  For other types, the parameter is ignored and should be set to <b>NULL</b>.


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



The new color context can be used in <a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a> to initialize the color context of a created bitmap.

When <i>space</i> is <a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE_CUSTOM</a>, <i>profile</i> and <i>profileSize</i> must be specified.  Otherwise, these parameters should be set to <b>NULL</b> and zero respectively.  When the space is D2D1_COLOR_SPACE_CUSTOM, the model field of the profile header is inspected to determine if this profile is sRGB or scRGB and the color space is updated respectively.  Otherwise the space remains custom.




## -see-also




<a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a>



<a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a>



<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

