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

# ITfTextInputProcessorEx::ActivateEx


## -description


The <b>ITfTextInputProcessorEx::ActivateEx</b> method activates a text service when a user session starts. If the text service implements <b>ITfTextInputProcessorEx</b> and <b>ActivateEx</b> is called, <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> will not be called.


## -parameters




### -param ptim [in]

[in] Pointer to the ITfThreadMgr interface for the thread manager that owns the text service.


### -param tid [in]

[in] Specifies the client identifier for the text service.


### -param dwFlags [in]

[in] The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_SECUREMODE"></a><a id="tf_tmae_securemode"></a><dl>
<dt><b>TF_TMAE_SECUREMODE</b></dt>
</dl>
</td>
<td width="60%">
A text service is activated as secure mode. A text service may not want to show the setting dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_COMLESS"></a><a id="tf_tmae_comless"></a><dl>
<dt><b>TF_TMAE_COMLESS</b></dt>
</dl>
</td>
<td width="60%">
A text service is activated as com less mode. TSF was activated without COM. COM may not be initialized or COM may be initialized as MTA.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_WOW16"></a><a id="tf_tmae_wow16"></a><dl>
<dt><b>TF_TMAE_WOW16</b></dt>
</dl>
</td>
<td width="60%">
The current thread is 16 bit task.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMAE_CONSOLE"></a><a id="tf_tmae_console"></a><dl>
<dt><b>TF_TMAE_CONSOLE</b></dt>
</dl>
</td>
<td width="60%">
A text service is activated for console usage.

</td>
</tr>
</table>
 


## -returns



The TSF manager ignores the return value of this method.



