---
UID: NF:msinkaut.IInkLineInfo.GetFormat
title: IInkLineInfo::GetFormat (msinkaut.h)
description: Returns the display properties currently set on the text ink object (tInk).
helpviewer_keywords: ["8f894963-7075-46f4-8809-82d1aa7e13e7","GetFormat","GetFormat method [Tablet PC]","GetFormat method [Tablet PC]","IInkLineInfo interface","IInkLineInfo interface [Tablet PC]","GetFormat method","IInkLineInfo.GetFormat","IInkLineInfo::GetFormat","msinkaut/IInkLineInfo::GetFormat","tablet.iinklineinfo_getformat"]
old-location: tablet\iinklineinfo_getformat.htm
tech.root: tablet
ms.assetid: 8f894963-7075-46f4-8809-82d1aa7e13e7
ms.date: 12/05/2018
ms.keywords: 8f894963-7075-46f4-8809-82d1aa7e13e7, GetFormat, GetFormat method [Tablet PC], GetFormat method [Tablet PC],IInkLineInfo interface, IInkLineInfo interface [Tablet PC],GetFormat method, IInkLineInfo.GetFormat, IInkLineInfo::GetFormat, msinkaut/IInkLineInfo::GetFormat, tablet.iinklineinfo_getformat
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkLineInfo::GetFormat
 - msinkaut/IInkLineInfo::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkLineInfo.GetFormat
---

# IInkLineInfo::GetFormat


## -description

Returns the display properties currently set on the text ink object (tInk).

## -parameters

### -param pim [out]

A pointer to an <a href="/windows/desktop/api/msinkaut/ns-msinkaut-inkmetric">INKMETRIC</a> structure that stores the display properties of the text ink object.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pim</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent">GetInkExtent Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo">IInkLineInfo</a>



<a href="/windows/desktop/api/msinkaut/ns-msinkaut-inkmetric">INKMETRIC Structure</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-setformat">SetFormat Method</a>