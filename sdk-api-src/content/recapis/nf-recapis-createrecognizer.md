---
UID: NF:recapis.CreateRecognizer
title: CreateRecognizer function (recapis.h)
author: windows-sdk-content
description: Creates a recognizer.
old-location: tablet\createrecognizer.htm
tech.root: tablet
ms.assetid: b4a5517e-d818-4d4d-a06f-3e0dcbcc52c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateRecognizer, CreateRecognizer function [Tablet PC], b4a5517e-d818-4d4d-a06f-3e0dcbcc52c6, recapis/CreateRecognizer, tablet.createrecognizer
ms.topic: function
f1_keywords: 
 - "recapis/CreateRecognizer"
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
 - CreateRecognizer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateRecognizer function


## -description



Creates a recognizer.




## -parameters




### -param pCLSID

CLSID of the recognizer. This value is created in the registry when you register the recognizer.


### -param phrec

Handle for the recognizer.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/registering-your-recognizer-dll">Registering Your Recognizer DLL</a>
 

 

