---
UID: NF:msinkaut.IInkExtendedProperties.Clear
title: IInkExtendedProperties::Clear (msinkaut.h)
description: Clears all of the IInkExtendedProperty objects from the IInkExtendedProperties collection.
helpviewer_keywords: ["Clear","Clear method [Tablet PC]","Clear method [Tablet PC]","IInkExtendedProperties interface","IInkExtendedProperties interface [Tablet PC]","Clear method","IInkExtendedProperties.Clear","IInkExtendedProperties::Clear","b5270e5c-51fa-4d1f-b4e0-9129c61bac88","msinkaut/IInkExtendedProperties::Clear","tablet.iinkextendedproperties_clear"]
old-location: tablet\iinkextendedproperties_clear.htm
tech.root: tablet
ms.assetid: b5270e5c-51fa-4d1f-b4e0-9129c61bac88
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Tablet PC], Clear method [Tablet PC],IInkExtendedProperties interface, IInkExtendedProperties interface [Tablet PC],Clear method, IInkExtendedProperties.Clear, IInkExtendedProperties::Clear, b5270e5c-51fa-4d1f-b4e0-9129c61bac88, msinkaut/IInkExtendedProperties::Clear, tablet.iinkextendedproperties_clear
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
 - IInkExtendedProperties::Clear
 - msinkaut/IInkExtendedProperties::Clear
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
 - IInkExtendedProperties.Clear
---

# IInkExtendedProperties::Clear


## -description

Clears all of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> objects from the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties</a> collection.



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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

To clear only one extended property at a time, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-remove">Remove</a> method of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties</a> collection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperties-remove">Remove Method [IInkExtendedProperties Interface]</a>
