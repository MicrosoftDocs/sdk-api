---
UID: NF:recapis.EndInkInput
title: EndInkInput function (recapis.h)
description: Indicates that no more ink will be added to the context.You cannot add strokes to the context after calling this function.
helpviewer_keywords: ["EndInkInput","EndInkInput function [Tablet PC]","e8aa252d-6b24-4864-9b3e-8edd30895303","recapis/EndInkInput","tablet.endinkinput"]
old-location: tablet\endinkinput.htm
tech.root: tablet
ms.assetid: e8aa252d-6b24-4864-9b3e-8edd30895303
ms.date: 11/06/2024
ms.keywords: EndInkInput, EndInkInput function [Tablet PC], e8aa252d-6b24-4864-9b3e-8edd30895303, recapis/EndInkInput, tablet.endinkinput
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
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
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EndInkInput
 - recapis/EndInkInput
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
 - EndInkInput
---

# EndInkInput function


## -description

Indicates that no more ink will be added to the context.

You cannot add strokes to the context after calling this function.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The recognizer context handle is invalid or null.

</td>
</tr>
</table>

## -remarks

The recognition results you receive after calling this function may be different from previous recognition results that were based on partial ink input.

The Ink Analysis API queries for the implementation of this method. If implemented, the InkAnalyzer will call it each time it performs an analysis operation. If not implemented, EndInkInput is never called. Therefore, you should only expose and implement this method if it is explicitly needed by your recognizer.

<div class="alert"><b>Note</b>  This function is not guaranteed to be called by all applications or operating system components, such as the Tablet PC Input Panel. Therefore, recognizers should not rely on it being called.</div>
<div> </div>

