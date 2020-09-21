---
UID: NS:msctf.TF_DA_COLOR
title: TF_DA_COLOR (msctf.h)
description: The TF_DA_COLOR structure contains color data used in the display attributes for a range of text.
helpviewer_keywords: ["TF_DA_COLOR","TF_DA_COLOR structure [Text Services Framework]","_tsf_tf_da_color_ref","msctf/TF_DA_COLOR","tsf.tf_da_color"]
old-location: tsf\tf_da_color.htm
tech.root: TSF
ms.assetid: 0ce8f941-c187-437f-8bad-f882e63b8421
ms.date: 12/05/2018
ms.keywords: TF_DA_COLOR, TF_DA_COLOR structure [Text Services Framework], _tsf_tf_da_color_ref, msctf/TF_DA_COLOR, tsf.tf_da_color
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
req.typenames: TF_DA_COLOR
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_DA_COLOR
 - msctf/TF_DA_COLOR
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
 - TF_DA_COLOR
---

# TF_DA_COLOR structure


## -description

The <b>TF_DA_COLOR</b> structure contains color data used in the display attributes for a range of text.

## -struct-fields

### -field type

Specifies the color type as defined in the <a href="/windows/win32/api/msctf/ne-msctf-tf_da_colortype">TF_DA_COLORTYPE</a> enumeration.

### -field nIndex

Specifies the color as a system color index as defined in <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>. This member is used only if <b>type</b> is equal to TF_CT_SYSCOLOR.

### -field cr

Specifies the color as an RGB value. This member is used only if <b>type</b> is equal to TF_CT_COLORREF.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>



<a href="/windows/win32/api/msctf/ne-msctf-tf_da_colortype">TF_DA_COLORTYPE
      </a>