---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateColorContext
title: ID2D1EffectContext::CreateColorContext
author: windows-sdk-content
description: Creates a color context from a color space.
old-location: direct2d\id2d1contextinternal_createcolorcontext.htm
tech.root: Direct2D
ms.assetid: FB06917B-091A-4429-83BA-DAEF26F654BE
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateColorContext, CreateColorContext method [Direct2D], CreateColorContext method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateColorContext method, ID2D1EffectContext.CreateColorContext, ID2D1EffectContext::CreateColorContext, d2d1effectauthor/ID2D1EffectContext::CreateColorContext, direct2d.id2d1contextinternal_createcolorcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
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
 - d2d1.dll
api_name:
 - ID2D1EffectContext.CreateColorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateColorContext


## -description


Creates a color context from a color space.  

If the color space is Custom, the context is initialized from the <i>profile</i> and <i>profileSize</i> parameters.

If the color space is not Custom, the context is       initialized with the profile bytes associated with the color space. The <i>profile</i> and <i>profileSize</i> parameters are ignored.


## -parameters




### -param space

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

The space  of color context to create.


### -param profile [in, optional]

Type: <b>const BYTE*</b>

A buffer containing the ICC profile bytes used to initialize the color context when <i>space</i> is <a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE_CUSTOM</a>.  For other types, the parameter is ignored and should be set to <b>NULL</b>.


### -param profileSize

Type: <b>UINT32</b>

The size in bytes of <i>Profile</i>.


### -param colorContext [out]

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to a new color context object.


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
 




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

