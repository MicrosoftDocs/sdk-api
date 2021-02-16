---
UID: NF:textstor.IAnchor.Compare
title: IAnchor::Compare (textstor.h)
description: The IAnchor::Compare method compares the relative position of two anchors within a text stream.
helpviewer_keywords: ["+1","-1","0","Compare","Compare method [Text Services Framework]","Compare method [Text Services Framework]","IAnchor interface","IAnchor interface [Text Services Framework]","Compare method","IAnchor.Compare","IAnchor::Compare","textstor/IAnchor::Compare","tsf.ianchor_compare"]
old-location: tsf\ianchor_compare.htm
tech.root: TSF
ms.assetid: 227ed0c0-0bdd-49af-b5dc-fdb69913b9c1
ms.date: 12/05/2018
ms.keywords: +1, -1, 0, Compare, Compare method [Text Services Framework], Compare method [Text Services Framework],IAnchor interface, IAnchor interface [Text Services Framework],Compare method, IAnchor.Compare, IAnchor::Compare, textstor/IAnchor::Compare, tsf.ianchor_compare
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IAnchor::Compare
 - textstor/IAnchor::Compare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.Compare
---

# IAnchor::Compare


## -description

The <b>IAnchor::Compare</b> method compares the relative position of two anchors within a text stream.

## -parameters

### -param paWith [in]

An anchor object to compare to the primary anchor. Used to determine the relative position of the two anchors.

### -param plResult [out]

Result of the comparison of the positions of the two anchors.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="-1"></a><dl>
<dt><b>-1</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned earlier in the text stream than <i>paWith.</i>

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned at the same location as <i>paWith.</i>

</td>
</tr>
<tr>
<td width="40%"><a id="_1"></a><dl>
<dt><b>+1</b></dt>
</dl>
</td>
<td width="60%">
The primary anchor is positioned later in the text stream than <i>paWith.</i>

</td>
</tr>
</table>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>paWith</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>plResult</i> is invalid.

</td>
</tr>
</table>

## -remarks

The value 0 is returned for <i>*plResult</i> only when the two anchors are in a single region. Anchor positions include the spaces between regions. If you only need to determine if the two anchors are positioned at the same location, <a href="/windows/desktop/api/textstor/nf-textstor-ianchor-isequal">IAnchor::IsEqual</a> is more efficient.

## -see-also

<a href="/windows/desktop/TSF/ranges">Anchors</a>



<a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-isequal">IAnchor::IsEqual
      </a>



<a href="/windows/desktop/TSF/ranges">Regions</a>