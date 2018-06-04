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

# ITfSourceSingle::UnadviseSingleSink


## -description




## -parameters




### -param tid [in]

Contains a <b>TfClientId</b> value that identifies the client.


### -param riid [in]

Identifies the type of advise sink to uninstall. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IID_ITfCleanupContextDurationSink"></a><a id="iid_itfcleanupcontextdurationsink"></a><a id="IID_ITFCLEANUPCONTEXTDURATIONSINK"></a><dl>
<dt><b>IID_ITfCleanupContextDurationSink</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the <a href="https://msdn.microsoft.com/2bbdc26a-5543-4de4-b347-2062be593c4b">ITfCleanupContextDurationSink</a> advise sink. Applies to: Text service

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfCleanupContextSink"></a><a id="iid_itfcleanupcontextsink"></a><a id="IID_ITFCLEANUPCONTEXTSINK"></a><dl>
<dt><b>IID_ITfCleanupContextSink</b></dt>
</dl>
</td>
<td width="60%">
Uninstalls the <a href="https://msdn.microsoft.com/f88ebef7-2796-4076-892f-28fac6e143de">ITfCleanupContextSink</a> advise sink. Applies to: Text service

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfFunctionProvider"></a><a id="iid_itffunctionprovider"></a><a id="IID_ITFFUNCTIONPROVIDER"></a><dl>
<dt><b>IID_ITfFunctionProvider</b></dt>
</dl>
</td>
<td width="60%">
Unregisters the client as a function provider. Applies to: Text Service and Application

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
The advise sink was successfully uninstalled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>tid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The advise sink is not installed.

</td>
</tr>
</table>
 



