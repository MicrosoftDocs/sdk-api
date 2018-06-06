---
UID: NS:textstor.TS_RUNINFO
title: TS_RUNINFO
author: windows-sdk-content
description: The TS_RUNINFO structure specifies the properties of text run data.
old-location: tsf\ts_runinfo.htm
old-project: TSF
ms.assetid: 601cd6b0-0064-4cd3-99cd-850104a861a5
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: TS_RUNINFO, TS_RUNINFO structure [Text Services Framework], _tsf_ts_runinfo_ref, textstor/TS_RUNINFO, tsf.ts_runinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_RUNINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_RUNINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 



