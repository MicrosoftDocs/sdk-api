---
UID: NF:d2d1_1.ID2D1ColorContext.GetProfile
title: ID2D1ColorContext::GetProfile
author: windows-sdk-content
description: Gets the color profile bytes for an ID2D1ColorContext.
old-location: direct2d\id2d1colorcontext_getprofile.htm
tech.root: Direct2D
ms.assetid: f6beae12-e02d-432b-b9d8-5e1206e3c482
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetProfile, GetProfile method [Direct2D], GetProfile method [Direct2D],ID2D1ColorContext interface, ID2D1ColorContext interface [Direct2D],GetProfile method, ID2D1ColorContext.GetProfile, ID2D1ColorContext::GetProfile, d2d1_1/ID2D1ColorContext::GetProfile, direct2d.id2d1colorcontext_getprofile
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
 - ID2D1ColorContext.GetProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1ColorContext.GetProfile
: 
---

# ID2D1ColorContext::GetProfile


## -description


Gets the color profile bytes for an <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>. 


## -parameters




### -param profile [out]

Type: <b>BYTE*</b>

When this method returns, contains the color profile.


### -param profileSize

Type: <b>UINT32</b>

The size of the <i>profile</i> buffer.


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
<td>D2DERR_INSUFFICIENT_BUFFER</td>
<td>The supplied buffer was too small to accomodate the data.</td>
</tr>
</table>
 




## -remarks



If <i>profileSize</i> is insufficient to store the entire profile, <i>profile</i> is zero-initialized before this method fails.




## -see-also




<a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a>



<a href="https://msdn.microsoft.com/7ab8bed5-c124-4e14-8a05-3a71f07f5fd1">ID2D1Bitmap1::GetColorContext</a>



<a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>



<a href="https://msdn.microsoft.com/ceae8c7d-80b5-4052-ac43-85f9802c209e">ID2D1ColorContext::GetProfileSize</a>
 

 

