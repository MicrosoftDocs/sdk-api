---
UID: NF:textstor.ITextStoreACP.FindNextAttrTransition
title: ITextStoreACP::FindNextAttrTransition (textstor.h)
description: The ITextStoreACP::FindNextAttrTransition method determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.
helpviewer_keywords: ["FindNextAttrTransition","FindNextAttrTransition method [Text Services Framework]","FindNextAttrTransition method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","FindNextAttrTransition method","ITextStoreACP.FindNextAttrTransition","ITextStoreACP::FindNextAttrTransition","TS_ATTR_FIND_BACKWARDS","TS_ATTR_FIND_WANT_OFFSET","_tsf_itextstoreacp_findnextattrtransition_ref","textstor/ITextStoreACP::FindNextAttrTransition","tsf.itextstoreacp_findnextattrtransition"]
old-location: tsf\itextstoreacp_findnextattrtransition.htm
tech.root: TSF
ms.assetid: f5917958-150e-48a5-9d0d-67240a88c232
ms.date: 12/05/2018
ms.keywords: FindNextAttrTransition, FindNextAttrTransition method [Text Services Framework], FindNextAttrTransition method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],FindNextAttrTransition method, ITextStoreACP.FindNextAttrTransition, ITextStoreACP::FindNextAttrTransition, TS_ATTR_FIND_BACKWARDS, TS_ATTR_FIND_WANT_OFFSET, _tsf_itextstoreacp_findnextattrtransition_ref, textstor/ITextStoreACP::FindNextAttrTransition, tsf.itextstoreacp_findnextattrtransition
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
 - ITextStoreACP::FindNextAttrTransition
 - textstor/ITextStoreACP::FindNextAttrTransition
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
 - ITextStoreACP.FindNextAttrTransition
---

# ITextStoreACP::FindNextAttrTransition


## -description

The <b>ITextStoreACP::FindNextAttrTransition</b> method determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.

## -parameters

### -param acpStart [in]

Specifies the character position to start the search for an attribute transition.

### -param acpHalt [in]

Specifies the character position to end the search for an attribute transition.

### -param cFilterAttrs [in]

Specifies the number of attributes to check.

### -param paFilterAttrs [in]

Pointer to the <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to check.

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
The method searches backward.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_OFFSET"></a><a id="ts_attr_find_want_offset"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <i>plFoundOffset</i> parameter receives the character offset of the attribute transition from <i>acpStart</i>.

</td>
</tr>
</table>

### -param pacpNext [out]

Receives the next character position to check for an attribute transition.

### -param pfFound [out]

Receives a Boolean value of <b>TRUE</b> if an attribute transition was found, otherwise <b>FALSE</b> is returned.

### -param plFoundOffset [out]

Receives the character position of the attribute transition (not ACP positions). If TS_ATTR_FIND_WANT_OFFSET flag is set in <i>dwFlags</i>, receives the character offset of the attribute transition from <i>acpStart</i>.

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
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The character positions specified are beyond the text in the document.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  If an application does not implement <b>ITextStoreACP::FindNextAttrTransition</b>, <a href="/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges">ITfReadOnlyProperty::EnumRanges</a> fails with E_FAIL.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>



<a href="/windows/desktop/TSF/ts-attr--constants">TS_ATTR_* Constants
      </a>