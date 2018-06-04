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
 



