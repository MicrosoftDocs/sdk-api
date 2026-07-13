---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0003
title: TsRunType (textstor.h)
description: Elements of the TsRunType enumeration specify if a text run is visible, hidden, or is a private data type embedded in the text run.
helpviewer_keywords: ["TS_RT_HIDDEN","TS_RT_OPAQUE","TS_RT_PLAIN","TsRunType","TsRunType enumeration [Text Services Framework]","_tsf_tsruntype_ref","textstor/TS_RT_HIDDEN","textstor/TS_RT_OPAQUE","textstor/TS_RT_PLAIN","textstor/TsRunType","tsf.tsruntype"]
old-location: tsf\tsruntype.htm
tech.root: TSF
ms.assetid: 47da6ff6-34c9-4c36-a254-ce8396723fcb
ms.date: 12/05/2018
ms.keywords: TS_RT_HIDDEN, TS_RT_OPAQUE, TS_RT_PLAIN, TsRunType, TsRunType enumeration [Text Services Framework], _tsf_tsruntype_ref, textstor/TS_RT_HIDDEN, textstor/TS_RT_OPAQUE, textstor/TS_RT_PLAIN, textstor/TsRunType, tsf.tsruntype
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TsRunType
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_textstor_0000_0000_0003
 - textstor/__MIDL___MIDL_itf_textstor_0000_0000_0003
 - TsRunType
 - textstor/TsRunType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TsRunType
---

# TsRunType enumeration


## -description

Elements of the <b>TsRunType</b> enumeration specify if a text run is visible, hidden, or is a private data type embedded in the text run.

## -enum-fields

### -field TS_RT_PLAIN:0

The text run is visible.

### -field TS_RT_HIDDEN

The text run is hidden.

### -field TS_RT_OPAQUE

The text run is a private data type embedded in the text run.

## -remarks

A text run is a collection of consecutive characters that is visible, hidden, or contains embedded data. For example, the text, Hello World in HTML might be &lt;b&gt;Hello &lt;/b&gt;&lt;i&gt;World&lt;/i&gt;. This text would be defined using the TsRunType as in the following.

<table>
<tr>
<th>Text Run</th>
<th>Value</th>
</tr>
<tr>
<td>&lt;b&gt;</td>
<td>TS_RT_HIDDEN</td>
</tr>
<tr>
<td>Hello&lt;space&gt;</td>
<td>TS_RT_PLAIN</td>
</tr>
<tr>
<td>&lt;/b&gt;</td>
<td>TS_RT_HIDDEN</td>
</tr>
<tr>
<td>&lt;i&gt;</td>
<td>TS_RT_HIDDEN</td>
</tr>
<tr>
<td>World</td>
<td>TS_RT_PLAIN</td>
</tr>
<tr>
<td>&lt;/i&gt;</td>
<td>TS_RT_HIDDEN</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext">ITextStoreACP::GetText</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_runinfo">TS_RUNINFO</a>
