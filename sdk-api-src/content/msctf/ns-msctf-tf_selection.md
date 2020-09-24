---
UID: NS:msctf.TF_SELECTION
title: TF_SELECTION (msctf.h)
description: The TF_SELECTION structure contains text selection data.
helpviewer_keywords: ["TF_SELECTION","TF_SELECTION structure [Text Services Framework]","_tsf_tf_selection_ref","msctf/TF_SELECTION","tsf.tf_selection"]
old-location: tsf\tf_selection.htm
tech.root: TSF
ms.assetid: c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54
ms.date: 12/05/2018
ms.keywords: TF_SELECTION, TF_SELECTION structure [Text Services Framework], _tsf_tf_selection_ref, msctf/TF_SELECTION, tsf.tf_selection
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
req.typenames: TF_SELECTION
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_SELECTION
 - msctf/TF_SELECTION
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
 - TF_SELECTION
---

# TF_SELECTION structure


## -description

The <b>TF_SELECTION</b> structure contains text selection data.

## -struct-fields

### -field range

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that specifies the selected text.

### -field style

A <a href="/windows/desktop/api/msctf/ns-msctf-tf_selectionstyle">TF_SELECTIONSTYLE</a> structure that contains selection data.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getselection">ITfContext::GetSelection
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-setselection">ITfContext::SetSelection
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_selectionstyle">TF_SELECTIONSTYLE
      </a>