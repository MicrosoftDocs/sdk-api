---
UID: NF:msctf.ITfReadOnlyProperty.EnumRanges
title: ITfReadOnlyProperty::EnumRanges (msctf.h)
description: ITfReadOnlyProperty::EnumRanges method
helpviewer_keywords: ["EnumRanges","EnumRanges method [Text Services Framework]","EnumRanges method [Text Services Framework]","ITfReadOnlyProperty interface","ITfReadOnlyProperty interface [Text Services Framework]","EnumRanges method","ITfReadOnlyProperty.EnumRanges","ITfReadOnlyProperty::EnumRanges","_tsf_itfreadonlyproperty_enumranges_ref","msctf/ITfReadOnlyProperty::EnumRanges","tsf.itfreadonlyproperty_enumranges"]
old-location: tsf\itfreadonlyproperty_enumranges.htm
tech.root: TSF
ms.assetid: 201c518b-f06f-4c4f-aa56-f8d21f477814
ms.date: 12/05/2018
ms.keywords: EnumRanges, EnumRanges method [Text Services Framework], EnumRanges method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],EnumRanges method, ITfReadOnlyProperty.EnumRanges, ITfReadOnlyProperty::EnumRanges, _tsf_itfreadonlyproperty_enumranges_ref, msctf/ITfReadOnlyProperty::EnumRanges, tsf.itfreadonlyproperty_enumranges
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfReadOnlyProperty::EnumRanges
 - msctf/ITfReadOnlyProperty::EnumRanges
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
 - ITfReadOnlyProperty.EnumRanges
---

# ITfReadOnlyProperty::EnumRanges


## -description

Obtains an enumeration of ranges that contain unique values of the property within the given range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfranges">IEnumTfRanges</a> interface pointer that receives the enumerator object. The caller must release this object when it is no longer required.

### -param pTargetRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that specifies the range to scan for unique property values. This parameter is optional and can be <b>NULL</b>. For more information, see the Remarks section.

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
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

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

<div class="alert"><b>Note</b>  If an application does not implement <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-findnextattrtransition">ITextStoreACP::FindNextAttrTransition</a>, ITfReadOnlyProperty::EnumRanges fails with E_FAIL.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only or read/write lock.

</td>
</tr>
</table>

## -remarks

<b>Note:</b> If an application does not implement <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-findnextattrtransition">ITextStoreACP::FindNextAttrTransition</a>, <b>ITfReadOnlyProperty::EnumRanges</b> fails with E_FAIL.

The enumerator obtained by this method will contain a range for each unique value, including empty values, of the specified property. For example, a hypothetical color property can be applied to the following marked up text:


``` syntax

COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text

```

When <b>ITfReadOnlyProperty::EnumRanges</b> is called with <i>pTargetRange</i> set to this range, the enumerator will contain five ranges.

<table>
<tr>
<th>Range Index</th>
<th>Color Property Value</th>
<th>Range Text</th>
</tr>
<tr>
<td>0</td>
<td>&lt;empty&gt;</td>
<td>"this "</td>
</tr>
<tr>
<td>1</td>
<td>R</td>
<td>"is"</td>
</tr>
<tr>
<td>2</td>
<td>&lt;empty&gt;</td>
<td>" some "</td>
</tr>
<tr>
<td>3</td>
<td>G</td>
<td>"colored "</td>
</tr>
<tr>
<td>4</td>
<td>&lt;empty&gt;</td>
<td>"text"</td>
</tr>
</table>
 

If <i>pTargetRange</i> is <b>NULL</b>, then the enumerator will begin and end with the first and last range that contains a non-empty property value in the context. Specifying <b>NULL</b> for <i>pTargetRange</i> in the above example would result in an enumerator with three ranges.

<table>
<tr>
<th>Range Index</th>
<th>Color Property Value</th>
<th>Text Within Range</th>
</tr>
<tr>
<td>0</td>
<td>R</td>
<td>"is"</td>
</tr>
<tr>
<td>1</td>
<td>&lt;empty&gt;</td>
<td>" some "</td>
</tr>
<tr>
<td>2</td>
<td>G</td>
<td>"colored "</td>
</tr>
</table>
 

The enumerated ranges will begin and end with the start and end anchors of <i>pTargetRange</i>, even if either anchor is positioned in the middle of a property.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-ienumtfranges">IEnumTfRanges</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a>
