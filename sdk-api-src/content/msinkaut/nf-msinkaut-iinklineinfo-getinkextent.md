---
UID: NF:msinkaut.IInkLineInfo.GetInkExtent
title: IInkLineInfo::GetInkExtent (msinkaut.h)
description: Specifies the display properties to set on the text ink object (tInk), and retrieves the width of the text ink object in HIMETRIC units.
helpviewer_keywords: ["0082b7d3-61b2-478a-a6dd-ba59c20b7e1d","GetInkExtent","GetInkExtent method [Tablet PC]","GetInkExtent method [Tablet PC]","IInkLineInfo interface","IInkLineInfo interface [Tablet PC]","GetInkExtent method","IInkLineInfo.GetInkExtent","IInkLineInfo::GetInkExtent","msinkaut/IInkLineInfo::GetInkExtent","tablet.iinklineinfo_getinkextent"]
old-location: tablet\iinklineinfo_getinkextent.htm
tech.root: tablet
ms.assetid: 0082b7d3-61b2-478a-a6dd-ba59c20b7e1d
ms.date: 12/05/2018
ms.keywords: 0082b7d3-61b2-478a-a6dd-ba59c20b7e1d, GetInkExtent, GetInkExtent method [Tablet PC], GetInkExtent method [Tablet PC],IInkLineInfo interface, IInkLineInfo interface [Tablet PC],GetInkExtent method, IInkLineInfo.GetInkExtent, IInkLineInfo::GetInkExtent, msinkaut/IInkLineInfo::GetInkExtent, tablet.iinklineinfo_getinkextent
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
 - IInkLineInfo::GetInkExtent
 - msinkaut/IInkLineInfo::GetInkExtent
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
 - IInkLineInfo.GetInkExtent
---

# IInkLineInfo::GetInkExtent


## -description

Specifies the display properties to set on the text ink object (tInk), and retrieves the width of the text ink object in HIMETRIC units.

## -parameters

### -param pim [in]

A pointer to an <a href="/windows/desktop/api/msinkaut/ns-msinkaut-inkmetric">INKMETRIC</a> structure, which contains the display properties to set on the text ink object, or <b>NULL</b>.

### -param pnWidth [out]

The width of the text ink object in HIMETRIC units.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pnWidth</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the operation. The display properties are not changed.

</td>
</tr>
</table>

## -remarks

If the <i>pim</i> parameter is <b>NULL</b>, then the display properties are not changed and the existing properties are used to calculate the extent of the text ink object; otherwise, the display properties are updated, and the extent is calculated from the new properties.

If the IMF_FONT_SELECTED_IN_HDC flag is set in the <i>pim</i> parameter, then the properties of the device context are applied to the ink; otherwise, the <a href="/windows/desktop/api/msinkaut/ns-msinkaut-inkmetric">INKMETRIC</a> settings of the text ink object are applied.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getformat">GetFormat Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo">IInkLineInfo</a>



<a href="/windows/desktop/api/msinkaut/ns-msinkaut-inkmetric">INKMETRIC Structure</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-setformat">SetFormat Method</a>