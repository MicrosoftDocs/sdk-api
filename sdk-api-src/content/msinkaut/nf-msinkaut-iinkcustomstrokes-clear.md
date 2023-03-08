---
UID: NF:msinkaut.IInkCustomStrokes.Clear
title: IInkCustomStrokes::Clear (msinkaut.h)
description: Clears all InkStrokes collections from the IInkCustomStrokes collection.
helpviewer_keywords: ["63ab20ee-f8ab-41ee-b85a-03d9a29dabc0","Clear","Clear method [Tablet PC]","Clear method [Tablet PC]","IInkCustomStrokes interface","IInkCustomStrokes interface [Tablet PC]","Clear method","IInkCustomStrokes.Clear","IInkCustomStrokes::Clear","msinkaut/IInkCustomStrokes::Clear","tablet.iinkcustomstrokes_clear"]
old-location: tablet\iinkcustomstrokes_clear.htm
tech.root: tablet
ms.assetid: 63ab20ee-f8ab-41ee-b85a-03d9a29dabc0
ms.date: 12/05/2018
ms.keywords: 63ab20ee-f8ab-41ee-b85a-03d9a29dabc0, Clear, Clear method [Tablet PC], Clear method [Tablet PC],IInkCustomStrokes interface, IInkCustomStrokes interface [Tablet PC],Clear method, IInkCustomStrokes.Clear, IInkCustomStrokes::Clear, msinkaut/IInkCustomStrokes::Clear, tablet.iinkcustomstrokes_clear
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
 - IInkCustomStrokes::Clear
 - msinkaut/IInkCustomStrokes::Clear
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
 - IInkCustomStrokes.Clear
---

# IInkCustomStrokes::Clear


## -description

Clears all <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections from the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

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
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes Interface</a>
