---
UID: NF:d2d1_1.ID2D1PrintControl.AddPage
title: ID2D1PrintControl::AddPage (d2d1_1.h)
description: Converts Direct2D primitives in the passed-in command list into a fixed page representation for use by the print subsystem.
helpviewer_keywords: ["AddPage","AddPage method [Direct2D]","AddPage method [Direct2D]","ID2D1PrintControl interface","ID2D1PrintControl interface [Direct2D]","AddPage method","ID2D1PrintControl.AddPage","ID2D1PrintControl::AddPage","d2d1_1/ID2D1PrintControl::AddPage","direct2d.id2d1printcontrol_addpage"]
old-location: direct2d\id2d1printcontrol_addpage.htm
tech.root: Direct2D
ms.assetid: 6B157EE8-36C8-4054-9975-3D3B82B3D013
ms.date: 12/05/2018
ms.keywords: AddPage, AddPage method [Direct2D], AddPage method [Direct2D],ID2D1PrintControl interface, ID2D1PrintControl interface [Direct2D],AddPage method, ID2D1PrintControl.AddPage, ID2D1PrintControl::AddPage, d2d1_1/ID2D1PrintControl::AddPage, direct2d.id2d1printcontrol_addpage
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1PrintControl::AddPage
 - d2d1_1/ID2D1PrintControl::AddPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1PrintControl.AddPage
---

## -description

Converts Direct2D primitives in the passed-in command list into a fixed page representation for use  by the print subsystem.

## -parameters

### -param commandList [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a>*</b>

The command list that contains the rendering operations.

### -param pageSize

Type: <b><a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f">D2D_SIZE_F</a></b>

The size of the page to add, in DIPs (1 inch == 96 DIP). If the print driver doesn't respond to this parameter, then you can use *pagePrintTicketStream* instead.

### -param pagePrintTicketStream [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The print ticket stream. You can use this to modify properties of the current page; for example, paper size or orientation.

### -param tag1 [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

Contains the first label for subsequent drawing operations. This parameter is passed uninitialized. If NULL is specified, no value is retrieved for this parameter.

### -param tag2 [out, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

Contains the second label for subsequent drawing operations. This parameter is passed uninitialized. If NULL is specified, no value is retrieved for this parameter.

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
<tr>
<td>D2DERR_PRINT_JOB_CLOSED</td>
<td>The print job is already finished.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a>
