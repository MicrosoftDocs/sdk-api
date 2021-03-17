---
UID: NS:textserv.CHANGENOTIFY
title: CHANGENOTIFY (textserv.h)
description: Contains information that is associated with an EN_CHANGE notification code. A windowless rich edit control sends this notification to its host window when the content of the control changes.
helpviewer_keywords: ["CHANGENOTIFY","CHANGENOTIFY structure [Windows Controls]","CN_GENERIC","CN_NEWREDO","CN_NEWUNDO","CN_TEXTCHANGED","controls.changenotify","textserv/CHANGENOTIFY"]
old-location: controls\changenotify.htm
tech.root: Controls
ms.assetid: F4756754-EF22-430F-B9EE-F4270EBBEF33
ms.date: 12/05/2018
ms.keywords: CHANGENOTIFY, CHANGENOTIFY structure [Windows Controls], CN_GENERIC, CN_NEWREDO, CN_NEWUNDO, CN_TEXTCHANGED, controls.changenotify, textserv/CHANGENOTIFY
req.header: textserv.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHANGENOTIFY
 - textserv/CHANGENOTIFY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textserv.h
api_name:
 - CHANGENOTIFY
---

# CHANGENOTIFY structure


## -description

Contains information that is associated with an <a href="/windows/desktop/Controls/en-change--rich-edit-control-">EN_CHANGE</a> notification code. A windowless rich edit control sends this notification to its host window when the content of the control changes.

## -struct-fields

### -field dwChangeType

The type of change that occurred. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CN_GENERIC"></a><a id="cn_generic"></a><dl>
<dt><b>CN_GENERIC</b></dt>
</dl>
</td>
<td width="60%">
No significant change occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_NEWREDO"></a><a id="cn_newredo"></a><dl>
<dt><b>CN_NEWREDO</b></dt>
</dl>
</td>
<td width="60%">
A new redo action was added.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_NEWUNDO"></a><a id="cn_newundo"></a><dl>
<dt><b>CN_NEWUNDO</b></dt>
</dl>
</td>
<td width="60%">
A new undo action was added.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_TEXTCHANGED"></a><a id="cn_textchanged"></a><dl>
<dt><b>CN_TEXTCHANGED</b></dt>
</dl>
</td>
<td width="60%">
The text changed.

</td>
</tr>
</table>

### -field pvCookieData

Cookie for the undo action 
										that is associated with the change.

## -see-also

<a href="/windows/desktop/Controls/en-change--rich-edit-control-">EN_CHANGE</a>