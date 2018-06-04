---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

