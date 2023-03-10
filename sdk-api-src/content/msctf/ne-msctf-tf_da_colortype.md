---
UID: NE:msctf.__MIDL___MIDL_itf_msctf_0000_0070_0002
title: TF_DA_COLORTYPE (msctf.h)
description: Elements of the TF_DA_COLORTYPE enumeration specify the format of the color contained in the TF_DA_COLOR structure.
helpviewer_keywords: ["TF_CT_COLORREF","TF_CT_NONE","TF_CT_SYSCOLOR","TF_DA_COLORTYPE","TF_DA_COLORTYPE enumeration [Text Services Framework]","_tsf_tf_da_colortype_ref","msctf/TF_CT_COLORREF","msctf/TF_CT_NONE","msctf/TF_CT_SYSCOLOR","msctf/TF_DA_COLORTYPE","tsf.tf_da_colortype"]
old-location: tsf\tf_da_colortype.htm
tech.root: TSF
ms.assetid: f692e188-d2f4-453b-a576-c6c05fd5f02a
ms.date: 12/05/2018
ms.keywords: TF_CT_COLORREF, TF_CT_NONE, TF_CT_SYSCOLOR, TF_DA_COLORTYPE, TF_DA_COLORTYPE enumeration [Text Services Framework], _tsf_tf_da_colortype_ref, msctf/TF_CT_COLORREF, msctf/TF_CT_NONE, msctf/TF_CT_SYSCOLOR, msctf/TF_DA_COLORTYPE, tsf.tf_da_colortype
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
req.typenames: TF_DA_COLORTYPE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msctf_0000_0070_0002
 - msctf/__MIDL___MIDL_itf_msctf_0000_0070_0002
 - TF_DA_COLORTYPE
 - msctf/TF_DA_COLORTYPE
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
 - TF_DA_COLORTYPE
---

# TF_DA_COLORTYPE enumeration


## -description

Elements of the <b>TF_DA_COLORTYPE</b> enumeration specify the format of the color contained in the <a href="/windows/desktop/api/msctf/ns-msctf-tf_da_color">TF_DA_COLOR</a> structure.

## -enum-fields

### -field TF_CT_NONE:0

The structure contains no color data.

### -field TF_CT_SYSCOLOR:1

The color is specified as a system color index. For more information about the system color indexes, see <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>.

### -field TF_CT_COLORREF:2

The color is specified as an RGB value.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_da_color">TF_DA_COLOR
      </a>
