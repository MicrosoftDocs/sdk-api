---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateResourceTexture
title: ID2D1EffectContext::CreateResourceTexture
author: windows-sdk-content
description: Creates or finds the given resource texture, depending on whether a resource id is specified.
old-location: direct2d\id2d1contextinternal_createresourcetexture.htm
tech.root: direct2d
ms.assetid: 265888DA-03C2-42F0-92D8-FEB542F9BAA4
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CreateResourceTexture, CreateResourceTexture method [Direct2D], CreateResourceTexture method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateResourceTexture method, ID2D1EffectContext.CreateResourceTexture, ID2D1EffectContext::CreateResourceTexture, d2d1effectauthor/ID2D1EffectContext::CreateResourceTexture, direct2d.id2d1contextinternal_createresourcetexture
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateResourceTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateResourceTexture


## -description


Creates or finds the given resource texture, depending on whether a resource id is specified. It also optionally initializes the texture with the specified data.


## -parameters




### -param resourceId [in, optional]

Type: <b>const GUID*</b>

An optional pointer to the unique id that identifies the lookup table.


### -param resourceTextureProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/23a524a4-2226-497f-a20b-74cda924c429">D2D1_RESOURCE_TEXTURE_PROPERTIES</a>*</b>

The properties used to create the resource texture.


### -param data [in, optional]

Type: <b>const BYTE*</b>

The optional data to be loaded into the resource texture.



### -param strides [in, optional]

Type: <b>const UINT32*</b>

An optional pointer to the stride to advance through the resource texture, according to dimension.


### -param dataSize

Type: <b>UINT32</b>

The size, in bytes, of the data.


### -param resourceTexture [out]

Type: <b><a href="https://msdn.microsoft.com/516FFBB4-1908-4574-BD4A-884C142204CD">ID2D1ResourceTexture</a>**</b>

The returned texture that can be used as a resource in a Direct2D effect.


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
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

