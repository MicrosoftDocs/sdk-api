---
UID: NE:msctf.__MIDL___MIDL_itf_msctf_0000_0000_0001
title: TfAnchor (msctf.h)
description: Elements of the TfAnchor enumeration specify the start anchor or end anchor of an ITfRange object.
helpviewer_keywords: ["TF_ANCHOR_END","TF_ANCHOR_START","TfAnchor","TfAnchor enumeration [Text Services Framework]","_tsf_tfanchor_ref","msctf/TF_ANCHOR_END","msctf/TF_ANCHOR_START","msctf/TfAnchor","tsf.tfanchor"]
old-location: tsf\tfanchor.htm
tech.root: TSF
ms.assetid: d670666f-2915-4a23-b825-b534a015e37f
ms.date: 12/05/2018
ms.keywords: TF_ANCHOR_END, TF_ANCHOR_START, TfAnchor, TfAnchor enumeration [Text Services Framework], _tsf_tfanchor_ref, msctf/TF_ANCHOR_END, msctf/TF_ANCHOR_START, msctf/TfAnchor, tsf.tfanchor
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
req.typenames: TfAnchor
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msctf_0000_0000_0001
 - msctf/__MIDL___MIDL_itf_msctf_0000_0000_0001
 - TfAnchor
 - msctf/TfAnchor
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
 - TfAnchor
---

# TfAnchor enumeration


## -description

Elements of the <b>TfAnchor</b> enumeration specify the start anchor or end anchor of an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object.

## -enum-fields

### -field TF_ANCHOR_START:0

Specifies the start anchor of the <b>ITfRange</b> object.

### -field TF_ANCHOR_END:1

Specifies the end anchor of the <b>ITfRange</b> object.

## -remarks

A range refers to a span of text in a document. Each range is delimited by a start anchor and an end anchor.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_haltcond">TF_HALTCOND
      </a>
