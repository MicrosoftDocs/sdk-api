---
UID: NF:msctf.ITfCompositionView.GetOwnerClsid
title: ITfCompositionView::GetOwnerClsid (msctf.h)
description: ITfCompositionView::GetOwnerClsid method
helpviewer_keywords: ["GetOwnerClsid","GetOwnerClsid method [Text Services Framework]","GetOwnerClsid method [Text Services Framework]","ITfCompositionView interface","ITfCompositionView interface [Text Services Framework]","GetOwnerClsid method","ITfCompositionView.GetOwnerClsid","ITfCompositionView::GetOwnerClsid","_tsf_itfcompositionview_getownerclsid_ref","msctf/ITfCompositionView::GetOwnerClsid","tsf.itfcompositionview_getownerclsid"]
old-location: tsf\itfcompositionview_getownerclsid.htm
tech.root: TSF
ms.assetid: 1435e083-c6a1-491c-a7c2-7d2cb1d54508
ms.date: 12/05/2018
ms.keywords: GetOwnerClsid, GetOwnerClsid method [Text Services Framework], GetOwnerClsid method [Text Services Framework],ITfCompositionView interface, ITfCompositionView interface [Text Services Framework],GetOwnerClsid method, ITfCompositionView.GetOwnerClsid, ITfCompositionView::GetOwnerClsid, _tsf_itfcompositionview_getownerclsid_ref, msctf/ITfCompositionView::GetOwnerClsid, tsf.itfcompositionview_getownerclsid
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
 - ITfCompositionView::GetOwnerClsid
 - msctf/ITfCompositionView::GetOwnerClsid
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
 - ITfCompositionView.GetOwnerClsid
---

# ITfCompositionView::GetOwnerClsid


## -description

Obtains the class identifier of the text service that created the composition object.

## -parameters

### -param pclsid [out]

Pointer to a CLSID that receives the class identifier of the text service that owns the composition.

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
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pclsid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The composition has been terminated.

</td>
</tr>
</table>

## -remarks

This method can be used to enable a text service to filter compositions that it does not own.

## -see-also

[ITfCompositionView interface](nn-msctf-itfcompositionview.md)

