---
UID: NF:tom.ITextDocument2.GetClientRect
title: ITextDocument2::GetClientRect (tom.h)
description: Retrieves the client rectangle of the rich edit control.
helpviewer_keywords: ["GetClientRect","GetClientRect method [Windows Controls]","GetClientRect method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetClientRect method","ITextDocument2.GetClientRect","ITextDocument2::GetClientRect","controls.itextdocument2_getclientrect","tom/ITextDocument2::GetClientRect","tomClientCoord","tomIncludeInset","tomTransform"]
old-location: controls\itextdocument2_getclientrect.htm
tech.root: Controls
ms.assetid: a5736c58-e402-421d-aa4a-79b65460b692
ms.date: 12/05/2018
ms.keywords: GetClientRect, GetClientRect method [Windows Controls], GetClientRect method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetClientRect method, ITextDocument2.GetClientRect, ITextDocument2::GetClientRect, controls.itextdocument2_getclientrect, tom/ITextDocument2::GetClientRect, tomClientCoord, tomIncludeInset, tomTransform
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextDocument2::GetClientRect
 - tom/ITextDocument2::GetClientRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetClientRect
---

# ITextDocument2::GetClientRect


## -description

Retrieves the client rectangle of the rich edit control.

## -parameters

### -param Type [in]

Type: <b>long</b>

The client rectangle retrieval options. It can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomClientCoord"></a><a id="tomclientcoord"></a><a id="TOMCLIENTCOORD"></a><dl>
<dt><b>tomClientCoord</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the rectangle in client coordinates. If this value isn't specified, the function retrieves screen coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="tomIncludeInset"></a><a id="tomincludeinset"></a><a id="TOMINCLUDEINSET"></a><dl>
<dt><b>tomIncludeInset</b></dt>
</dl>
</td>
<td width="60%">
Add left and top insets to the left and top coordinates of the client rectangle, and subtract right and bottom insets from the right and bottom coordinates. 

</td>
</tr>
<tr>
<td width="40%"><a id="tomTransform"></a><a id="tomtransform"></a><a id="TOMTRANSFORM"></a><dl>
<dt><b>tomTransform</b></dt>
</dl>
</td>
<td width="60%">
Use a world transform (XFORM) provided by the host application to transform the retrieved rectangle  coordinates.

</td>
</tr>
</table>

### -param pLeft [out]

Type: <b>long*</b>

The x-coordinate of the upper-left corner of the rectangle.

### -param pTop [out]

Type: <b>long*</b>

The y-coordinate of the upper-left corner of the rectangle.

### -param pRight [out]

Type: <b>long*</b>

The x-coordinate of the lower-right corner of the rectangle.

### -param pBottom [out]

Type: <b>long*</b>

The y-coordinate of the lower-right corner of the rectangle.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>