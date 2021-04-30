---
UID: NF:infotech.IITWordWheel.Count
title: IITWordWheel::Count (infotech.h)
description: Returns the number of entries in a word wheel.
helpviewer_keywords: ["Count","Count method [HTML Help Workshop]","Count method [HTML Help Workshop]","IITWordWheel interface","IITWordWheel interface [HTML Help Workshop]","Count method","IITWordWheel.Count","IITWordWheel::Count","htmlhelp.iitwordwheel_count","infotech/IITWordWheel::Count","refIITWordWheelCount"]
old-location: htmlhelp\iitwordwheel_count.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheelcount.htm
ms.date: 12/05/2018
ms.keywords: Count, Count method [HTML Help Workshop], Count method [HTML Help Workshop],IITWordWheel interface, IITWordWheel interface [HTML Help Workshop],Count method, IITWordWheel.Count, IITWordWheel::Count, htmlhelp.iitwordwheel_count, infotech/IITWordWheel::Count, refIITWordWheelCount
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IITWordWheel::Count
 - infotech/IITWordWheel::Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITWordWheel.Count
---

# IITWordWheel::Count


## -description

Returns the number of entries in a word wheel.

## -parameters

### -param pcEntries [in]

Number of entries in word wheel.

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
The count was successfully returned.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTOPEN</b></dt>
</dl>
</td>
<td width="60%">
The word wheel has not been opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcEntries</i> parameter was an invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitwordwheel">IITWordWheel</a>