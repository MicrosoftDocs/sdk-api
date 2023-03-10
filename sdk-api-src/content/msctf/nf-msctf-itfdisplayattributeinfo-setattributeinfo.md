---
UID: NF:msctf.ITfDisplayAttributeInfo.SetAttributeInfo
title: ITfDisplayAttributeInfo::SetAttributeInfo (msctf.h)
description: ITfDisplayAttributeInfo::SetAttributeInfo method
helpviewer_keywords: ["ITfDisplayAttributeInfo interface [Text Services Framework]","SetAttributeInfo method","ITfDisplayAttributeInfo.SetAttributeInfo","ITfDisplayAttributeInfo::SetAttributeInfo","SetAttributeInfo","SetAttributeInfo method [Text Services Framework]","SetAttributeInfo method [Text Services Framework]","ITfDisplayAttributeInfo interface","_tsf_itfdisplayattributeinfo_setattributeinfo_ref","msctf/ITfDisplayAttributeInfo::SetAttributeInfo","tsf.itfdisplayattributeinfo_setattributeinfo"]
old-location: tsf\itfdisplayattributeinfo_setattributeinfo.htm
tech.root: TSF
ms.assetid: 3e9a472c-7992-48fc-be47-993f6d53f043
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeInfo interface [Text Services Framework],SetAttributeInfo method, ITfDisplayAttributeInfo.SetAttributeInfo, ITfDisplayAttributeInfo::SetAttributeInfo, SetAttributeInfo, SetAttributeInfo method [Text Services Framework], SetAttributeInfo method [Text Services Framework],ITfDisplayAttributeInfo interface, _tsf_itfdisplayattributeinfo_setattributeinfo_ref, msctf/ITfDisplayAttributeInfo::SetAttributeInfo, tsf.itfdisplayattributeinfo_setattributeinfo
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
 - ITfDisplayAttributeInfo::SetAttributeInfo
 - msctf/ITfDisplayAttributeInfo::SetAttributeInfo
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
 - ITfDisplayAttributeInfo.SetAttributeInfo
---

# ITfDisplayAttributeInfo::SetAttributeInfo


## -description

Sets the new attribute data.

## -parameters

### -param pda [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_displayattribute">TF_DISPLAYATTRIBUTE</a> structure that contains the new display attribute data.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The display attribute provider does not support attribute modification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pda</i> is invalid.

</td>
</tr>
</table>

## -remarks

The implementation of this method should not call <a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-onupdateinfo">ITfDisplayAttributeMgr::OnUpdateInfo</a> in response to this method. The caller must do so. This avoids redundant notifications if more than one attribute is modified. The caller must eventually call <b>ITfDisplayAttributeMgr::OnUpdateInfo</b> so that other clients will receive an attribute update notification.

## -see-also

[ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md), [ITfDisplayAttributeMgr::OnUpdateInfo](nf-msctf-itfdisplayattributemgr-onupdateinfo.md), [TF_DISPLAYATTRIBUTE structure](ns-msctf-tf_displayattribute.md), [ITfDisplayAttributeInfo::GetAttributeInfo](nf-msctf-itfdisplayattributeinfo-getattributeinfo.md)