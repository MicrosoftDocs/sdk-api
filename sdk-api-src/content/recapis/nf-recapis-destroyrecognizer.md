---
UID: NF:recapis.DestroyRecognizer
title: DestroyRecognizer function (recapis.h)
author: windows-sdk-content
description: Destroys a recognizer.
old-location: tablet\destroyrecognizer.htm
tech.root: tablet
ms.assetid: ffd66ab7-fc11-407e-aedc-267271ecb32c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DestroyRecognizer, DestroyRecognizer function [Tablet PC], ffd66ab7-fc11-407e-aedc-267271ecb32c, recapis/DestroyRecognizer, tablet.destroyrecognizer
ms.topic: function
f1_keywords: 
 - "recapis/DestroyRecognizer"
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
 - DestroyRecognizer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 



