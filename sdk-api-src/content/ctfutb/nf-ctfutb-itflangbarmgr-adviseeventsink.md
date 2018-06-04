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

# ITfLangBarMgr::AdviseEventSink


## -description


The <b>ITfLangBarMgr::AdviseEventSink</b> method advises a sink about a language bar event.


## -parameters




### -param pSink [in]

Sink object to advise about the event.


### -param hwnd [in]

Reserved; must be <b>NULL</b>.


### -param dwFlags [in]

Reserved; must be 0.


### -param pdwCookie [in]

Pointer to an identifier for the connection.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSink</i> is invalid.

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
 




## -remarks



<i>pdwCookie</i> receives an identifier that should be passed to <a href="https://msdn.microsoft.com/29dc5276-04fa-4219-a64d-10d775d73fdd">ITfLangBarMgr::UnadviseEventSink</a> when the event sink is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/60bd765f-0846-47f5-af1b-bc8e72720841">ITfLangBarMgr</a>



<a href="https://msdn.microsoft.com/29dc5276-04fa-4219-a64d-10d775d73fdd">ITfLangBarMgr::UnadviseEventSink
      </a>



<a href="https://msdn.microsoft.com/fd43b4c3-80bb-4118-a880-bdea07022c95">Thread Manager</a>
 

 

