---
UID: NS:msctf.TF_HALTCOND
title: TF_HALTCOND (msctf.h)
description: The TF_HALTCOND structure is used to contain conditions of a range shift.
helpviewer_keywords: ["TF_HALTCOND","TF_HALTCOND structure [Text Services Framework]","_tsf_tf_haltcond_ref","msctf/TF_HALTCOND","tsf.tf_haltcond"]
old-location: tsf\tf_haltcond.htm
tech.root: TSF
ms.assetid: 055f3228-1e3b-4e31-9035-e509a98016a8
ms.date: 12/05/2018
ms.keywords: TF_HALTCOND, TF_HALTCOND structure [Text Services Framework], _tsf_tf_haltcond_ref, msctf/TF_HALTCOND, tsf.tf_haltcond
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TF_HALTCOND
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_HALTCOND
 - msctf/TF_HALTCOND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_HALTCOND
---

# TF_HALTCOND structure


## -description

The <b>TF_HALTCOND</b> structure is used to contain conditions of a range shift.

## -struct-fields

### -field pHaltRange

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that halts the shift. If the range shift encounters this range during the shift, the shift halts. This member can be <b>NULL</b>.

### -field aHaltPos

Contains one of the <a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor</a> values that specifies which anchor of <b>pHaltRange</b> the anchor will get shifted to if <b>pHaltRange</b> is encountered during the range shift. This member is ignored if <b>pHaltRange</b> is <b>NULL</b>.

### -field dwFlags

Contains a set of flags that modify the behavior of the range shift. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_HF_OBJECT</td>
<td>The range shift halts if an embedded object is encountered.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftend">ITfRange::ShiftEnd
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstart">ITfRange::ShiftStart
      </a>



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
      </a>