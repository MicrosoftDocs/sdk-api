---
UID: NE:msctf.__MIDL_ITfRange_0001
title: TfGravity (msctf.h)
description: Elements of the TfGravity enumeration specify the type of gravity associated with the anchor of an ITfRange object.
helpviewer_keywords: ["TF_GRAVITY_BACKWARD","TF_GRAVITY_FORWARD","TfGravity","TfGravity enumeration [Text Services Framework]","_tsf_tfgravity_ref","msctf/TF_GRAVITY_BACKWARD","msctf/TF_GRAVITY_FORWARD","msctf/TfGravity","tsf.tfgravity"]
old-location: tsf\tfgravity.htm
tech.root: TSF
ms.assetid: 844925e7-4c3e-41e7-b560-586c85530cb4
ms.date: 12/05/2018
ms.keywords: TF_GRAVITY_BACKWARD, TF_GRAVITY_FORWARD, TfGravity, TfGravity enumeration [Text Services Framework], _tsf_tfgravity_ref, msctf/TF_GRAVITY_BACKWARD, msctf/TF_GRAVITY_FORWARD, msctf/TfGravity, tsf.tfgravity
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
req.typenames: TfGravity
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL_ITfRange_0001
 - msctf/__MIDL_ITfRange_0001
 - TfGravity
 - msctf/TfGravity
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
 - TfGravity
---

# TfGravity enumeration


## -description

Elements of the <b>TfGravity</b> enumeration specify the type of gravity associated with the anchor of an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object.

## -enum-fields

### -field TF_GRAVITY_BACKWARD:0

The anchor has backward gravity.

### -field TF_GRAVITY_FORWARD:1

The anchor has forward gravity.

## -remarks

For more information about anchor gravity, see <a href="/windows/desktop/TSF/ranges">Anchor Gravity</a>.

## -see-also

<a href="/windows/desktop/TSF/ranges">Anchor Gravity</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-getgravity">ITfRange::GetGravity</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-setgravity">ITfRange::SetGravity</a>
