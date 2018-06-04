---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISimpleFrameSite::PostMessageFilter


## -description


Sends the simple frame site a message that is received by a control's own window after the control has processed the message.


## -parameters




### -param hWnd [in]

A handle of the control window receiving the message.


### -param msg [in]

The message received by the simple frame site.


### -param wp [in]

The <b>WPARAM</b> of the message.


### -param lp [in]

The <b>LPARAM</b> of the message.


### -param plResult [out]

 A pointer to the variable that receives the result of the message processing.


### -param dwCookie [in]

The value that was returned by <a href="https://msdn.microsoft.com/f308ea77-12e7-450b-8b0f-252f1d240388">ISimpleFrameSite::PreMessageFilter</a> through its <i>pdwCookie</i> parameter.


## -returns



This method can return the following values.

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
The site processed the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The site did not process the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The site does not filter any messages.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ccddeae4-14fc-47df-a612-83d48a479b48">ISimpleFrameSite</a>
 

 

