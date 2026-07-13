---
UID: NF:msctf.ITfProperty.FindRange
title: ITfProperty::FindRange (msctf.h)
description: ITfProperty::FindRange method
helpviewer_keywords: ["FindRange","FindRange method [Text Services Framework]","FindRange method [Text Services Framework]","ITfProperty interface","ITfProperty interface [Text Services Framework]","FindRange method","ITfProperty.FindRange","ITfProperty::FindRange","_tsf_itfproperty_findrange_ref","msctf/ITfProperty::FindRange","tsf.itfproperty_findrange"]
old-location: tsf\itfproperty_findrange.htm
tech.root: TSF
ms.assetid: 08e9c9c1-768b-406c-96ae-e0776b59344d
ms.date: 12/05/2018
ms.keywords: FindRange, FindRange method [Text Services Framework], FindRange method [Text Services Framework],ITfProperty interface, ITfProperty interface [Text Services Framework],FindRange method, ITfProperty.FindRange, ITfProperty::FindRange, _tsf_itfproperty_findrange_ref, msctf/ITfProperty::FindRange, tsf.itfproperty_findrange
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
 - ITfProperty::FindRange
 - msctf/ITfProperty::FindRange
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
 - ITfProperty.FindRange
---

# ITfProperty::FindRange


## -description

Obtains a range that covers the text that contains a non-empty value for the property.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the point to obtain the property range for. The point will either be the start anchor or end anchor of this range, based upon the value of <i>aPos</i>.

### -param ppRange [out]

Pointer to an <b>ITfRange</b> interface pointer that receives the requested range object.

### -param aPos [in]

Contains one of the <a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor</a> values which specifies which anchor of <i>pRange</i> is used as the point to obtain the property range for.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>pRange</i> is not over, or adjacent to, the property. <i>ppRange</i> receives <b>NULL</b>.

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

This method obtains a range of text that contains a non-empty value for the property. If the property has no value at the specified point, <i>ppRange</i> receives <b>NULL</b> and the method returns S_FALSE. In the following example, if <i>aPos</i> contains TF_ANCHOR_START, the returned range would contain "is". If <i>aPos</i> contains TF_ANCHOR_END, the method would return S_FALSE because the property does not exist at the end point of the range.


``` syntax

COLOR: RRRRR   RR          GGGGGGGG
TEXT:  this <a>is som</a>e colored text

```

If <i>aPos</i> contains TF_ANCHOR_START, this method ignores property ranges that end immediately before the start anchor. Likewise, if <i>aPos</i> contains TF_ANCHOR_END, this method ignores property ranges that start immediately after the end anchor. In the following example, if <i>aPos</i> contains TF_ANCHOR_START, the returned range would contain "colored " and not "some " because the R value property ends at the start anchor point and the G value property begins at the start anchor. If <i>aPos</i> contains TF_ANCHOR_END, the returned range would contain "colored " and not "text".


``` syntax

COLOR:         RRRRR   GGGGGGGG    BBBB
TEXT:  this is some <a>colored </a>text

```


## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor</a>
