---
UID: NF:msctf.ITfDisplayAttributeInfo.Reset
title: ITfDisplayAttributeInfo::Reset (msctf.h)
description: ITfDisplayAttributeInfo::Reset method
helpviewer_keywords: ["ITfDisplayAttributeInfo interface [Text Services Framework]","Reset method","ITfDisplayAttributeInfo.Reset","ITfDisplayAttributeInfo::Reset","Reset","Reset method [Text Services Framework]","Reset method [Text Services Framework]","ITfDisplayAttributeInfo interface","_tsf_itfdisplayattributeinfo_reset_ref","msctf/ITfDisplayAttributeInfo::Reset","tsf.itfdisplayattributeinfo_reset"]
old-location: tsf\itfdisplayattributeinfo_reset.htm
tech.root: TSF
ms.assetid: f7a95bb4-a2f1-4734-8a71-286591544984
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeInfo interface [Text Services Framework],Reset method, ITfDisplayAttributeInfo.Reset, ITfDisplayAttributeInfo::Reset, Reset, Reset method [Text Services Framework], Reset method [Text Services Framework],ITfDisplayAttributeInfo interface, _tsf_itfdisplayattributeinfo_reset_ref, msctf/ITfDisplayAttributeInfo::Reset, tsf.itfdisplayattributeinfo_reset
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
 - ITfDisplayAttributeInfo::Reset
 - msctf/ITfDisplayAttributeInfo::Reset
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
 - ITfDisplayAttributeInfo.Reset
---

# ITfDisplayAttributeInfo::Reset


## -description

Resets the display attribute data to its default value.



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
</table>

## -remarks

The implementation of this method should not call <a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-onupdateinfo">ITfDisplayAttributeMgr::OnUpdateInfo</a> in response to this method. The caller must do so. This avoids redundant notifications if more than one attribute is modified. The caller must eventually call <b>ITfDisplayAttributeMgr::OnUpdateInfo</b> so that other clients will receive an attribute update notification.

## -see-also

[ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md), [ITfDisplayAttributeMgr::OnUpdateInfo](nf-msctf-itfdisplayattributemgr-onupdateinfo.md),
