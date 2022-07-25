---
UID: NS:msctf.TF_SELECTIONSTYLE
title: TF_SELECTIONSTYLE (msctf.h)
description: The TF_SELECTIONSTYLE structure represents the style of a selection.
helpviewer_keywords: ["TF_SELECTIONSTYLE","TF_SELECTIONSTYLE structure [Text Services Framework]","_tsf_tf_selectionstyle_ref","msctf/TF_SELECTIONSTYLE","tsf.tf_selectionstyle"]
old-location: tsf\tf_selectionstyle.htm
tech.root: TSF
ms.assetid: 3a38172b-611b-445f-be24-ea2a19178255
ms.date: 12/05/2018
ms.keywords: TF_SELECTIONSTYLE, TF_SELECTIONSTYLE structure [Text Services Framework], _tsf_tf_selectionstyle_ref, msctf/TF_SELECTIONSTYLE, tsf.tf_selectionstyle
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
req.typenames: TF_SELECTIONSTYLE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_SELECTIONSTYLE
 - msctf/TF_SELECTIONSTYLE
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
 - TF_SELECTIONSTYLE
---

# TF_SELECTIONSTYLE structure


## -description

The <b>TF_SELECTIONSTYLE</b> structure represents the style of a selection.

## -struct-fields

### -field ase

Specifies the active end of the selection. For more information, see <a href="/windows/win32/api/msctf/ne-msctf-tfactiveselend">TfActiveSelEnd</a>.

### -field fInterimChar

Indicates if the selection is an interim character. If this value is nonzero, then the selection is an interim character and <b>ase</b> will be TF_AE_NONE. If this value is zero, the selection is not an interim character.

## -remarks

An interim character selection spans exactly one character and is visually represented as a solid rectangle that is usually flashing. This is a standard UI element of Korean and some Chinese character compositions. <b>fInterimChar</b> is an indication that a specific character is composed. <b>fInterimChar</b> can only be nonzero for a single selection. In this case, there will be no caret because the highlight replaces it.

## -see-also

<a href="/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION
      </a>



<a href="/windows/win32/api/msctf/ne-msctf-tfactiveselend">TfActiveSelEnd
      </a>