---
UID: NF:recapis.DestroyContext
title: DestroyContext function (recapis.h)
description: Destroys a recognizer context.
helpviewer_keywords: ["DestroyContext","DestroyContext function [Tablet PC]","b0d90728-6934-4727-b553-c6058acfa0ec","recapis/DestroyContext","tablet.destroycontext"]
old-location: tablet\destroycontext.htm
tech.root: tablet
ms.assetid: b0d90728-6934-4727-b553-c6058acfa0ec
ms.date: 12/05/2018
ms.keywords: DestroyContext, DestroyContext function [Tablet PC], b0d90728-6934-4727-b553-c6058acfa0ec, recapis/DestroyContext, tablet.destroycontext
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
 - DestroyContext
 - recapis/DestroyContext
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
 - DestroyContext
---

# DestroyContext function


## -description

Destroys a recognizer context.

## -parameters

### -param hrc

Handle to the recognizer context.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

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
</table>

