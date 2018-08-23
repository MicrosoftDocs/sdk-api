---
UID: NF:d2d1effectauthor.ID2D1EffectContext.FindResourceTexture
title: ID2D1EffectContext::FindResourceTexture
author: windows-sdk-content
description: Finds the given resource texture if it has already been created with ID2D1EffectContext::CreateResourceTexture with the same GUID.
old-location: direct2d\id2d1effectcontext_findresourcetexture.htm
old-project: direct2d
ms.assetid: 7E205798-A9E1-4213-925B-7A5DF918F60E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FindResourceTexture, FindResourceTexture method [Direct2D], FindResourceTexture method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],FindResourceTexture method, ID2D1EffectContext.FindResourceTexture, ID2D1EffectContext::FindResourceTexture, d2d1effectauthor/ID2D1EffectContext::FindResourceTexture, direct2d.id2d1effectcontext_findresourcetexture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_VERTEX_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.FindResourceTexture
product: Windows
targetos: Windows
req.lib: D2D1.lib
req.dll: 
req.irql: 
---

# ID2D1EffectContext::FindResourceTexture


## -description


Finds the given resource texture if it has already been created with <a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">ID2D1EffectContext::CreateResourceTexture</a> with the same GUID.


## -parameters




### -param resourceId [in]

Type: <b>const GUID*</b>

The unique id that identifies the resource texture.


### -param resourceTexture [out]

Type: <b><a href="https://msdn.microsoft.com/516FFBB4-1908-4574-BD4A-884C142204CD">ID2D1ResourceTexture</a>**</b>

The returned texture that can be used as a resource in a Direct2D effect.


## -returns



Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


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
<td>E_NOTFOUND</td>
<td>The requested resource texture was not found.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

