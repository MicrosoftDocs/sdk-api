---
UID: NF:recapis.SetGuide
title: SetGuide function (recapis.h)
description: Sets the recognition guide to use for boxed or lined input. You must call this function before you add strokes to the context.
helpviewer_keywords: ["3ca3c743-83f9-46b0-851a-cba6e4ed980a","SetGuide","SetGuide function [Tablet PC]","recapis/SetGuide","tablet.setguide"]
old-location: tablet\setguide.htm
tech.root: tablet
ms.assetid: 3ca3c743-83f9-46b0-851a-cba6e4ed980a
ms.date: 12/05/2018
ms.keywords: 3ca3c743-83f9-46b0-851a-cba6e4ed980a, SetGuide, SetGuide function [Tablet PC], recapis/SetGuide, tablet.setguide
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
 - SetGuide
 - recapis/SetGuide
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
 - SetGuide
---

# SetGuide function


## -description

Sets the recognition guide to use for boxed or lined input. You must call this function before you add strokes to the context.

## -parameters

### -param hrc

Handle to the recognizer context.

### -param pGuide

Guide to use for box or line input. Setting this parameter to <b>NULL</b> means that the context has no guide. This is the default and means the recognizer is in free input mode. For guide details, see the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_guide">RECO_GUIDE</a> structure.

### -param iIndex

Index value to use for the first box or line in the context.

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
The context is invalid or one of the parameters is an invalid pointer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Attempted to set a recognition mode (free, lined, boxed, and so on) that is not supported by the recognizer, or the RECO_GUIDE field values are illegal (negative heights or widths, for example).

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
<dt><b>TPC_E_OUT_OF_ORDER_CALL</b></dt>
</dl>
</td>
<td width="60%">
Attempted to set guide when there was already some ink in the reco context, or, in the case of recognizers of East Asian characters, <a href="/windows/desktop/api/recapis/nf-recapis-setcacmode">SetCACMode</a> was called previously.

</td>
</tr>
</table>

## -remarks

Guide boxes are numbered based on the <i>iIntex</i> value.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getguide">GetGuide Function</a>



<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_guide">RECO_GUIDE Structure</a>