---
UID: NE:msctf.__MIDL_ITfContext_0001
title: TfActiveSelEnd (msctf.h)
author: windows-sdk-content
description: Elements of the TfActiveSelEnd enumeration specify which end of a selected range of text is active.
old-location: tsf\tfactiveselend.htm
tech.root: TSF
ms.assetid: bb89f0b4-a0b4-42ea-8467-6fc634e37aec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TF_AE_END, TF_AE_NONE, TF_AE_START, TfActiveSelEnd, TfActiveSelEnd enumeration [Text Services Framework], _tsf_tfactiveselend_ref, msctf/TF_AE_END, msctf/TF_AE_NONE, msctf/TF_AE_START, msctf/TfActiveSelEnd, tsf.tfactiveselend
ms.topic: enum
f1_keywords: 
 - "msctf/TfActiveSelEnd"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TfActiveSelEnd
targetos: Windows
req.typenames: TfActiveSelEnd
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# TfActiveSelEnd enumeration


## -description


Elements of the <b>TfActiveSelEnd</b> enumeration specify which end of a selected range of text is active.


## -enum-fields




### -field TF_AE_NONE

The selected range has no active end. This is typical for selected ranges other than the default selected range.


### -field TF_AE_START

The active end is at the start of the selected range.


### -field TF_AE_END

The active end is at the end of the selected range.


## -remarks



The active end of a selected range is the end likely to respond to user actions. For example, in many applications, holding the SHIFT key down while using the arrow keys will change the selected range. The end of the selected range that moves is the active end of the selected range.

This enumeration is used in the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_selectionstyle">TF_SELECTIONSTYLE</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_selectionstyle">TF_SELECTIONSTYLE
      </a>
 

 

