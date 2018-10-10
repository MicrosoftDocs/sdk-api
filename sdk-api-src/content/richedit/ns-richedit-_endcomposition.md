---
UID: NS:richedit._endcomposition
title: "_endcomposition"
author: windows-sdk-content
description: Contains information about an EN_ENDCOMPOSITION notification code from a rich edit control.
old-location: controls\endcompositionnotify.htm
tech.root: Controls
ms.assetid: 5C137287-01B5-4E2E-A62E-F340A29CD8D7
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ECN_ENDCOMPOSITION, ECN_NEWTEXT, ENDCOMPOSITIONNOTIFY, ENDCOMPOSITIONNOTIFY structure [Windows Controls], _endcomposition, controls.endcompositionnotify, richedit/ENDCOMPOSITIONNOTIFY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - ENDCOMPOSITIONNOTIFY
product: Windows
targetos: Windows
req.typenames: ENDCOMPOSITIONNOTIFY
req.redist: 
---

# _endcomposition structure


## -description


Contains information about an EN_ENDCOMPOSITION notification code from a rich edit control. 




## -struct-fields




### -field nmhdr

The <b>code</b> member of this structure identifies the notification code being sent. 


### -field dwCode

Indicates the state of the composition. This member is one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ECN_ENDCOMPOSITION"></a><a id="ecn_endcomposition"></a><dl>
<dt><b>ECN_ENDCOMPOSITION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The composition is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="ECN_NEWTEXT"></a><a id="ecn_newtext"></a><dl>
<dt><b>ECN_NEWTEXT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
There are new characters in the composition.

</td>
</tr>
</table>
 

