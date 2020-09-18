---
UID: NF:textstor.ITextStoreAnchor.FindNextAttrTransition
title: ITextStoreAnchor::FindNextAttrTransition (textstor.h)
description: The ITextStoreAnchor::FindNextAttrTransition method finds the location in the text stream where a transition occurs in an attribute value. The specified attribute to check is application-dependent.
helpviewer_keywords: ["FindNextAttrTransition","FindNextAttrTransition method [Text Services Framework]","FindNextAttrTransition method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","FindNextAttrTransition method","ITextStoreAnchor.FindNextAttrTransition","ITextStoreAnchor::FindNextAttrTransition","TS_ATTR_FIND_BACKWARDS","TS_ATTR_FIND_UPDATESTART","TS_ATTR_FIND_WANT_OFFSET","textstor/ITextStoreAnchor::FindNextAttrTransition","tsf.itextstoreanchor_findnextattrtransition"]
old-location: tsf\itextstoreanchor_findnextattrtransition.htm
tech.root: TSF
ms.assetid: 9bb21a4a-047e-4347-93b3-9c41cd2c20b7
ms.date: 12/05/2018
ms.keywords: FindNextAttrTransition, FindNextAttrTransition method [Text Services Framework], FindNextAttrTransition method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],FindNextAttrTransition method, ITextStoreAnchor.FindNextAttrTransition, ITextStoreAnchor::FindNextAttrTransition, TS_ATTR_FIND_BACKWARDS, TS_ATTR_FIND_UPDATESTART, TS_ATTR_FIND_WANT_OFFSET, textstor/ITextStoreAnchor::FindNextAttrTransition, tsf.itextstoreanchor_findnextattrtransition
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor::FindNextAttrTransition
 - textstor/ITextStoreAnchor::FindNextAttrTransition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.FindNextAttrTransition
---

# ITextStoreAnchor::FindNextAttrTransition


## -description

The <b>ITextStoreAnchor::FindNextAttrTransition</b> method finds the location in the text stream where a transition occurs in an attribute value. The specified attribute to check is application-dependent.

## -parameters

### -param paStart [in]

Pointer to the anchor position at the start of a range to search for an attribute transition.

### -param paHalt [in]

Pointer to the anchor position at the end of a range to search for an attribute transition.

### -param cFilterAttrs [in]

Specifies the number of attributes to check.

### -param paFilterAttrs [in]

Pointer to the <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to check. Pre-defined attributes are given in tsattrs.h.

### -param dwFlags [in]

Specifies the direction to search for an attribute transition. By default, the method searches forward.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_BACKWARDS"></a><a id="ts_attr_find_backwards"></a><dl>
<dt><b>TS_ATTR_FIND_BACKWARDS</b></dt>
</dl>
</td>
<td width="60%">
The method searches backward in the text stream.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_UPDATESTART"></a><a id="ts_attr_find_updatestart"></a><dl>
<dt><b>TS_ATTR_FIND_UPDATESTART</b></dt>
</dl>
</td>
<td width="60%">
The method positions the input anchor <i>paStart</i> at the next attribute transition, if one is found. Otherwise the input anchor is not modified.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_OFFSET"></a><a id="ts_attr_find_want_offset"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <i>plFoundOffset</i> parameter receives the character offset of the attribute transition from <i>paStart</i>.

</td>
</tr>
</table>

### -param pfFound [out]

Receives a Boolean value of <b>TRUE</b> if an attribute transition was found, otherwise <b>FALSE</b> is returned.

### -param plFoundOffset [out]

Receives the character offset of the attribute transition from the start anchor <i>paStart</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paStart</i> and/or <i>paHalt</i> are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The character positions specified are beyond the text in the document.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>



<a href="/windows/desktop/TSF/ts-attr--constants">TS_ATTR_* Constants
      </a>