---
UID: NF:recapis.CloneContext
title: CloneContext function (recapis.h)
description: Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original.
helpviewer_keywords: ["0a16d012-1d88-4dfb-a1a0-44a842d9ee1d","CloneContext","CloneContext function [Tablet PC]","recapis/CloneContext","tablet.clonecontext"]
old-location: tablet\clonecontext.htm
tech.root: tablet
ms.assetid: 0a16d012-1d88-4dfb-a1a0-44a842d9ee1d
ms.date: 12/05/2018
ms.keywords: 0a16d012-1d88-4dfb-a1a0-44a842d9ee1d, CloneContext, CloneContext function [Tablet PC], recapis/CloneContext, tablet.clonecontext
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
 - CloneContext
 - recapis/CloneContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - CloneContext
---

# CloneContext function


## -description

Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pCloneHrc

The new recognizer context.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCloneHrc</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

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

## -remarks

The settings  for this context include the recognition guide, character Autocomplete mode, and any factoids that improve the recognition results. An example of a factoid may include whether the ink is a phone number, a name, or a URL. The TextContext and Wordlists are preserved in the new context.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-resetcontext">ResetContext Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-settextcontext">SetTextContext Function</a>