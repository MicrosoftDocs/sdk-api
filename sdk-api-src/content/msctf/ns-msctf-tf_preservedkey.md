---
UID: NS:msctf.TF_PRESERVEDKEY
title: TF_PRESERVEDKEY (msctf.h)
description: The TF_PRESERVEDKEY structure represents a preserved key.
helpviewer_keywords: ["TF_PRESERVEDKEY","TF_PRESERVEDKEY structure [Text Services Framework]","_tsf_tf_preservedkey_ref","msctf/TF_PRESERVEDKEY","tsf.tf_preservedkey"]
old-location: tsf\tf_preservedkey.htm
tech.root: TSF
ms.assetid: 95d37e94-3991-49c9-bddf-4183a69d49b9
ms.date: 12/05/2018
ms.keywords: TF_PRESERVEDKEY, TF_PRESERVEDKEY structure [Text Services Framework], _tsf_tf_preservedkey_ref, msctf/TF_PRESERVEDKEY, tsf.tf_preservedkey
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
req.typenames: TF_PRESERVEDKEY
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_PRESERVEDKEY
 - msctf/TF_PRESERVEDKEY
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
 - TF_PRESERVEDKEY
---

# TF_PRESERVEDKEY structure


## -description

The <b>TF_PRESERVEDKEY</b> structure represents a preserved key.

## -struct-fields

### -field uVKey

Virtual key code of the keyboard shortcut.

### -field uModifiers

Modifies the preserved key. This can be zero or a combination of one or more of the <a href="/windows/desktop/TSF/tf-mod--constants">TF_MOD_* constants</a>.

## -remarks

Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.

## -see-also

<a href="/windows/desktop/TSF/tf-mod--constants">TF_MOD_* constants
      </a>