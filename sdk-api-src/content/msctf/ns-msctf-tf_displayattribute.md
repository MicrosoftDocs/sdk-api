---
UID: NS:msctf.TF_DISPLAYATTRIBUTE
title: TF_DISPLAYATTRIBUTE (msctf.h)
description: The TF_DISPLAYATTRIBUTE structure contains display attribute data for rendering text.
helpviewer_keywords: ["TF_DISPLAYATTRIBUTE","TF_DISPLAYATTRIBUTE structure [Text Services Framework]","_tsf_tf_displayattribute_ref","msctf/TF_DISPLAYATTRIBUTE","tsf.tf_displayattribute"]
old-location: tsf\tf_displayattribute.htm
tech.root: TSF
ms.assetid: 29faaa22-ea03-4a2e-a035-7979e2a89fc9
ms.date: 12/05/2018
ms.keywords: TF_DISPLAYATTRIBUTE, TF_DISPLAYATTRIBUTE structure [Text Services Framework], _tsf_tf_displayattribute_ref, msctf/TF_DISPLAYATTRIBUTE, tsf.tf_displayattribute
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
req.typenames: TF_DISPLAYATTRIBUTE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_DISPLAYATTRIBUTE
 - msctf/TF_DISPLAYATTRIBUTE
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
 - TF_DISPLAYATTRIBUTE
---

# TF_DISPLAYATTRIBUTE structure


## -description

The <b>TF_DISPLAYATTRIBUTE</b> structure contains display attribute data for rendering text.

## -struct-fields

### -field crText

Contains a <a href="/windows/desktop/api/msctf/ns-msctf-tf_da_color">TF_DA_COLOR</a> structure that defines the text foreground color.

### -field crBk

Contains a <b>TF_DA_COLOR</b> structure that defines the text background color.

### -field lsStyle

Contains a <a href="/windows/win32/api/msctf/ne-msctf-tf_da_linestyle">TF_DA_LINESTYLE</a> enumeration value that defines the underline style.

### -field fBoldLine

A BOOL value that specifies if the underline should be bold or normal weight. If this value is nonzero, the underline should be bold. If this value is zero, the underline should be normal.

### -field crLine

Contains a <b>TF_DA_COLOR</b> structure that defines the color of the underline.

### -field bAttr

Contains a <a href="/windows/win32/api/msctf/ne-msctf-tf_da_attr_info">TF_DA_ATTR_INFO</a> value that defines text conversion display attribute data.

## -see-also

<a href="/windows/win32/api/msctf/ne-msctf-tf_da_attr_info">TF_DA_ATTR_INFO
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_da_color">TF_DA_COLOR
      </a>



<a href="/windows/win32/api/msctf/ne-msctf-tf_da_linestyle">TF_DA_LINESTYLE
      </a>