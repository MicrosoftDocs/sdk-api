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

# ISimpleFrameSite::PreMessageFilter


## -description


Provides a site with the opportunity to process a message that is received by a control's own window before the control itself does any processing.


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


### -param pdwCookie [out]

A pointer to the variable that will be passed to <a href="https://msdn.microsoft.com/b9725ef9-16e0-4574-9b94-826814a396be">ISimpleFrameSite::PostMessageFilter</a> if it is called later. This parameter should only contain allocated data if this method returns S_OK so it will also receive a call to <b>PostMessageFilter</b> which can free the allocation. The caller is not in any way responsible for anything returned in this parameter.


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
The simple frame site will not use the message in this filter so more processing can take place.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The site has processed the message and no further processing should occur.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The site does not do any message filtering, indicating that PostMessageFilter need not be called later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>plResult</i> or <i>pdwCookie</i> is not valid.

</td>
</tr>
</table>
 




## -remarks



Successful return values indicate whether the site wishes to allow further processing. S_OK indicates further processing, whereas S_FALSE means do not process further. S_OK also indicates that the control must later call <a href="https://msdn.microsoft.com/b9725ef9-16e0-4574-9b94-826814a396be">PostMessageFilter</a>.





## -see-also




<a href="https://msdn.microsoft.com/ccddeae4-14fc-47df-a612-83d48a479b48">ISimpleFrameSite</a>
 

 

