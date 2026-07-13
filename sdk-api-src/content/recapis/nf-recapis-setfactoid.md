---
UID: NF:recapis.SetFactoid
title: SetFactoid function (recapis.h)
description: Specifies the factoid a recognizer uses to constrain its search for the result.You specify a factoid if an input field is of a known type, such as if the input field contains a date.
helpviewer_keywords: ["SetFactoid","SetFactoid function [Tablet PC]","f805b364-1e7b-4995-bda9-47bff87fcdfa","recapis/SetFactoid","tablet.setfactoid"]
old-location: tablet\setfactoid.htm
tech.root: tablet
ms.assetid: f805b364-1e7b-4995-bda9-47bff87fcdfa
ms.date: 12/05/2018
ms.keywords: SetFactoid, SetFactoid function [Tablet PC], f805b364-1e7b-4995-bda9-47bff87fcdfa, recapis/SetFactoid, tablet.setfactoid
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
 - SetFactoid
 - recapis/SetFactoid
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
 - SetFactoid
---

# SetFactoid function


## -description

Specifies the factoid a recognizer uses to constrain its search for the result.

You specify a factoid if an input field is of a known type, such as if the input field contains a date. You call this function before processing the ink for the first time. Therefore, call the <b>SetFactoid</b> function before calling the <a href="/windows/desktop/api/recapis/nf-recapis-process">Process</a> function.

## -parameters

### -param hrc

Handle to the recognizer context.

### -param cwcFactoid

Number of characters in <i>pwcFactoid</i>.

### -param pwcFactoid

Identifies the factoid to use on the recognizer context. The string is not <b>NULL</b>-terminated.

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
<dt><b>TPC_E_INVALID_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The specified factoid is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_OUT_OF_ORDER_CALL</b></dt>
</dl>
</td>
<td width="60%">
You must call the SetFactoid function before calling the Process function.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support this function.

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
The context contains an invalid value.

</td>
</tr>
</table>

## -remarks

For a list of factoids that can be passed in the <i>cwcFactoid</i> parameter, see <a href="/windows/desktop/tablet/supported-factoids-from-version-1">Supported Factoids from Version 1</a>. The DEFAULT factoid listed in that topic is not a valid value to pass to <b>SetFactoid</b>; the Tablet PC Platform API's internally convert DEFAULT to <b>NULL</b> before calling the <b>SetFactoid</b> function.

It is recommended that you limit the length of the factoid string to no more than 32768 characters.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-setflags">SetFlags Function</a>