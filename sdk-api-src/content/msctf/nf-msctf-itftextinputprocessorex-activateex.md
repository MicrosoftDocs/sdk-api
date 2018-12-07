---
UID: NF:msctf.ITfTextInputProcessorEx.ActivateEx
title: ITfTextInputProcessorEx::ActivateEx
author: windows-sdk-content
description: The ITfTextInputProcessorEx::ActivateEx method activates a text service when a user session starts. If the text service implements ITfTextInputProcessorEx and ActivateEx is called, ITfTextInputProcessor::Activate will not be called.
old-location: tsf\itftextinputprocessorex_activateex.htm
tech.root: TSF
ms.assetid: b628e803-ea94-4e69-9919-94e4164d5b36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ActivateEx, ActivateEx method [Text Services Framework], ActivateEx method [Text Services Framework],ITfTextInputProcessorEx interface, ITfTextInputProcessorEx interface [Text Services Framework],ActivateEx method, ITfTextInputProcessorEx.ActivateEx, ITfTextInputProcessorEx::ActivateEx, TF_TMAE_COMLESS, TF_TMAE_CONSOLE, TF_TMAE_SECUREMODE, TF_TMAE_WOW16, msctf/ITfTextInputProcessorEx::ActivateEx, tsf.itftextinputprocessorex_activateex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfTextInputProcessorEx.ActivateEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
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



