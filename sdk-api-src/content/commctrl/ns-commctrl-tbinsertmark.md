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

# TBINSERTMARK structure


## -description


Contains information on the insertion mark in a toolbar control. 


## -struct-fields




### -field iButton

Type: <b>int</b>

Zero-based index of the insertion mark. If this member is -1, there is no insertion mark. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Defines where the insertion mark is in relation to 
					<b>iButton</b>. This can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the left of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_AFTER"></a><a id="tbimht_after"></a><dl>
<dt><b>TBIMHT_AFTER</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the right of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_BACKGROUND"></a><a id="tbimht_background"></a><dl>
<dt><b>TBIMHT_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is on the background of the toolbar. This flag is only used with the <a href="https://msdn.microsoft.com/65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e">TB_INSERTMARKHITTEST</a> message. 

</td>
</tr>
</table>
 

