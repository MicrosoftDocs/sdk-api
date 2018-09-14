---
UID: NF:recapis.CreateContext
title: CreateContext function
author: windows-sdk-content
description: Creates a recognizer context.
old-location: tablet\createcontext.htm
tech.root: tablet
ms.assetid: 4e599157-93d6-486f-9498-899e5b53f24b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 4e599157-93d6-486f-9498-899e5b53f24b, CreateContext, CreateContext function [Tablet PC], recapis/CreateContext, tablet.createcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - CreateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateContext function


## -description



Creates a recognizer context.




## -parameters




### -param hrec

Handle to the recognizer.


### -param phrc

Pointer to the recognizer context.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

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
 



