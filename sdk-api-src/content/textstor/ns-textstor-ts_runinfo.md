---
UID: NS:textstor.TS_RUNINFO
title: TS_RUNINFO (textstor.h)
description: The TS_RUNINFO structure specifies the properties of text run data.
helpviewer_keywords: ["TS_RUNINFO","TS_RUNINFO structure [Text Services Framework]","_tsf_ts_runinfo_ref","textstor/TS_RUNINFO","tsf.ts_runinfo"]
old-location: tsf\ts_runinfo.htm
tech.root: TSF
ms.assetid: 601cd6b0-0064-4cd3-99cd-850104a861a5
ms.date: 12/05/2018
ms.keywords: TS_RUNINFO, TS_RUNINFO structure [Text Services Framework], _tsf_ts_runinfo_ref, textstor/TS_RUNINFO, tsf.ts_runinfo
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
req.typenames: TS_RUNINFO
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_RUNINFO
 - textstor/TS_RUNINFO
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
 - TS_RUNINFO
---

# TS_RUNINFO structure


## -description

The <b>TS_RUNINFO</b> structure specifies the properties of text run data.

## -struct-fields

### -field uCount

Specifies the number of characters in the text run.

### -field type

Specifies the text run type. If this parameter is TS_RT_PLAIN, the text run is visible. If this parameter is TS_RT_HIDDEN, the text run is hidden. If this parameter is TS_RT_OPAQUE, the text run is a private data type embedded in the text by application or text service that implements the ITextStore interface.

## -remarks

A text run is a collection of consecutive visible, hidden, or embedded characters. For example, the text, Hello World in HTML might be &lt;b&gt;Hello &lt;/b&gt;&lt;i&gt;World&lt;/i&gt;. This text is represented in the TS_RUNINFO structure as follows.

<table>
<tr>
<th>Text Run</th>
<th>uCount</th>
<th>TsRunType</th>
</tr>
<tr>
<td>&lt;b&gt;</td>
<td>3</td>
<td>TS_RT_HIDDEN</td>
</tr>
<tr>
<td>Hello&lt;space&gt;</td>
<td>5</td>
<td>TS_RT_PLAIN</td>
</tr>
<tr>
<td>&lt;/b&gt;&lt;i&gt;</td>
<td>7</td>
<td>TS_RT_HIDDEN</td>
</tr>
<tr>
<td>World</td>
<td>5</td>
<td>TS_RT_PLAIN</td>
</tr>
<tr>
<td>&lt;/i&gt;</td>
<td>4</td>
<td>TS_RT_HIDDEN</td>
</tr>
</table>

