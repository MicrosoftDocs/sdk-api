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

# ITfThreadMgr2::GetActiveFlags


## -description


Gets the active flags of the calling thread.


## -parameters




### -param lpdwFlags [out]

The pointer to the DWORD value to receives the active flags of TSF.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_NOACTIVATETIP"></a><a id="tf_tmf_noactivatetip"></a><dl>
<dt><b>TF_TMF_NOACTIVATETIP</b></dt>
</dl>
</td>
<td width="60%">
TSF was activated with the TF_TMAE_NOACTIVATETIP flag.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_SECUREMODE"></a><a id="tf_tmf_securemode"></a><dl>
<dt><b>TF_TMF_SECUREMODE</b></dt>
</dl>
</td>
<td width="60%">
TSF is running as secure mode.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_UIELEMENTENABLEDONLY"></a><a id="tf_tmf_uielementenabledonly"></a><dl>
<dt><b>TF_TMF_UIELEMENTENABLEDONLY</b></dt>
</dl>
</td>
<td width="60%">
TSF is running with text services that support only UIElement.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_COMLESS"></a><a id="tf_tmf_comless"></a><dl>
<dt><b>TF_TMF_COMLESS</b></dt>
</dl>
</td>
<td width="60%">
TSF is running without COM.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_WOW16"></a><a id="tf_tmf_wow16"></a><dl>
<dt><b>TF_TMF_WOW16</b></dt>
</dl>
</td>
<td width="60%">
TSF is running in 16bit task.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_CONSOLE"></a><a id="tf_tmf_console"></a><dl>
<dt><b>TF_TMF_CONSOLE</b></dt>
</dl>
</td>
<td width="60%">
TSF is running for console.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_IMMERSIVEMODE"></a><a id="tf_tmf_immersivemode"></a><dl>
<dt><b>TF_TMF_IMMERSIVEMODE</b></dt>
</dl>
</td>
<td width="60%">
TSF is active in a Windows Store app.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TMF_ACTIVATED"></a><a id="tf_tmf_activated"></a><dl>
<dt><b>TF_TMF_ACTIVATED</b></dt>
</dl>
</td>
<td width="60%">
TSF is active.

</td>
</tr>
</table>
 


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
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 

