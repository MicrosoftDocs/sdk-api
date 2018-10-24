---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateColorContextFromFilename
title: ID2D1EffectContext::CreateColorContextFromFilename
author: windows-sdk-content
description: Creates a color context by loading it from the specified filename. The profile bytes are the contents of the file specified by filename.
old-location: direct2d\id2d1contextinternal_createcolorcontextfromfilename.htm
tech.root: Direct2D
ms.assetid: 84B12901-48B1-4FA9-8C81-1CEA70CF2824
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CreateColorContextFromFilename, CreateColorContextFromFilename method [Direct2D], CreateColorContextFromFilename method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateColorContextFromFilename method, ID2D1EffectContext.CreateColorContextFromFilename, ID2D1EffectContext::CreateColorContextFromFilename, d2d1effectauthor/ID2D1EffectContext::CreateColorContextFromFilename, direct2d.id2d1contextinternal_createcolorcontextfromfilename
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
 - ID2D1EffectContext.CreateColorContextFromFilename
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateColorContextFromFilename


## -description


Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>filename</i>.


## -parameters




### -param filename

Type: <b>PCWSTR</b>

The path to the file containing the profile bytes to initialize the color context with.


### -param colorContext [out]

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to a new color context.


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
 

 

