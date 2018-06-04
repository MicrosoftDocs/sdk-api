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

# ITextRange::ScrollIntoView


## -description


Scrolls the specified range into view. 


## -parameters




### -param Value






#### - bStart

Type: <b>long</b>

Flag specifying the end to scroll into view. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomEnd"></a><a id="tomend"></a><a id="TOMEND"></a><dl>
<dt><b><a href="tomconstants.htm">tomEnd</a></b></dt>
</dl>
</td>
<td width="60%">
Scrolls the end character position to appear on the bottom line.

</td>
</tr>
<tr>
<td width="40%"><a id="tomStart"></a><a id="tomstart"></a><a id="TOMSTART"></a><dl>
<dt><b><a href="tomconstants.htm">tomStart</a></b></dt>
</dl>
</td>
<td width="60%">
Scrolls the start character position to appear on the top line. (Default value).

</td>
</tr>
<tr>
<td width="40%"><a id="tomNoUpScroll"></a><a id="tomnoupscroll"></a><a id="TOMNOUPSCROLL"></a><dl>
<dt><b><a href="tomconstants.htm">tomNoUpScroll</a></b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="tomNoVpScroll"></a><a id="tomnovpscroll"></a><a id="TOMNOVPSCROLL"></a><dl>
<dt><b><a href="tomconstants.htm">tomNoVpScroll</a></b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

