---
UID: NF:recapis.ResetContext
title: ResetContext function (recapis.h)
description: Deletes the current ink and recognition results from the context.The current settings of the recognizer context are preserved.
helpviewer_keywords: ["92446aca-e611-42b2-8b55-2d1c47ccaa5c","ResetContext","ResetContext function [Tablet PC]","recapis/ResetContext","tablet.resetcontext"]
old-location: tablet\resetcontext.htm
tech.root: tablet
ms.assetid: 92446aca-e611-42b2-8b55-2d1c47ccaa5c
ms.date: 11/06/2024
ms.keywords: 92446aca-e611-42b2-8b55-2d1c47ccaa5c, ResetContext, ResetContext function [Tablet PC], recapis/ResetContext, tablet.resetcontext
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResetContext
 - recapis/ResetContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport 
api_location:
 - recapis.h
 - inkobjcore.dll
 - mshwgst.dll
api_name:
 - ResetContext
---

# ResetContext function


## -description

Deletes the current ink and recognition results from the context.

The current settings of the recognizer context are preserved. The settings can include the recognition guide, character Autocomplete mode, and any recognition hints that improve recognition results. An example of a recognition hint may include whether a factoid is set indicating that the ink is a phone number, a name, or a URL. The TextContext and Wordlists are preserved in the context.

## -parameters

### -param hrc

The handle to the recognizer context.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-clonecontext">CloneContext Function</a>