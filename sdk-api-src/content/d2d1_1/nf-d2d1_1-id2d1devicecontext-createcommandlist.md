---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateCommandList
title: ID2D1DeviceContext::CreateCommandList (d2d1_1.h)
description: Creates a ID2D1CommandList object.
helpviewer_keywords: ["CreateCommandList","CreateCommandList method [Direct2D]","CreateCommandList method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateCommandList method","ID2D1DeviceContext.CreateCommandList","ID2D1DeviceContext::CreateCommandList","d2d1_1/ID2D1DeviceContext::CreateCommandList","direct2d.id2d1devicecontext_createcommandlist"]
old-location: direct2d\id2d1devicecontext_createcommandlist.htm
tech.root: Direct2D
ms.assetid: f34710dc-7845-457f-9b27-51ae937d9f74
ms.date: 12/05/2018
ms.keywords: CreateCommandList, CreateCommandList method [Direct2D], CreateCommandList method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateCommandList method, ID2D1DeviceContext.CreateCommandList, ID2D1DeviceContext::CreateCommandList, d2d1_1/ID2D1DeviceContext::CreateCommandList, direct2d.id2d1devicecontext_createcommandlist
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::CreateCommandList
 - d2d1_1/ID2D1DeviceContext::CreateCommandList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.CreateCommandList
---

# ID2D1DeviceContext::CreateCommandList


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> object.

## -parameters

### -param commandList [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a>**</b>

When this method returns, contains the address of a pointer to a command list.

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
</table>

## -remarks

A <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> can store Direct2D commands to be displayed later through <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a> or through an image brush.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>