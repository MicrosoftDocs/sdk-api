---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0003
title: "__MIDL___MIDL_itf_textstor_0000_0000_0003"
author: windows-sdk-content
description: Elements of the TsRunType enumeration specify if a text run is visible, hidden, or is a private data type embedded in the text run.
old-location: tsf\tsruntype.htm
old-project: TSF
ms.assetid: 47da6ff6-34c9-4c36-a254-ce8396723fcb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TS_RT_HIDDEN, TS_RT_OPAQUE, TS_RT_PLAIN, TsRunType, TsRunType enumeration [Text Services Framework], __MIDL___MIDL_itf_textstor_0000_0000_0003, _tsf_tsruntype_ref, textstor/TS_RT_HIDDEN, textstor/TS_RT_OPAQUE, textstor/TS_RT_PLAIN, textstor/TsRunType, tsf.tsruntype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: textstor.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TsRunType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_textstor_0000_0000_0003 enumeration


## -description


Elements of the <b>TsRunType</b> enumeration specify if a text run is visible, hidden, or is a private data type embedded in the text run.


## -enum-fields




### -field TS_RT_PLAIN

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




<a href="https://msdn.microsoft.com/c3788e8f-ddb8-4ad6-971c-e9c1f6a21f88">ITextStoreACP::GetText</a>



<a href="https://msdn.microsoft.com/601cd6b0-0064-4cd3-99cd-850104a861a5">TS_RUNINFO</a>
 

 

