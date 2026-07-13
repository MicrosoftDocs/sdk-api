---
UID: NF:recapis.DestroyRecognizer
title: DestroyRecognizer function (recapis.h)
description: Destroys a recognizer.
helpviewer_keywords: ["DestroyRecognizer","DestroyRecognizer function [Tablet PC]","ffd66ab7-fc11-407e-aedc-267271ecb32c","recapis/DestroyRecognizer","tablet.destroyrecognizer"]
old-location: tablet\destroyrecognizer.htm
tech.root: tablet
ms.assetid: ffd66ab7-fc11-407e-aedc-267271ecb32c
ms.date: 11/06/2024
ms.keywords: DestroyRecognizer, DestroyRecognizer function [Tablet PC], ffd66ab7-fc11-407e-aedc-267271ecb32c, recapis/DestroyRecognizer, tablet.destroyrecognizer
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
 - DestroyRecognizer
 - recapis/DestroyRecognizer
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
 - DestroyRecognizer
---

# DestroyRecognizer function


## -description

Destroys a recognizer.

## -parameters

### -param hrec

Handle to the recognizer.

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

