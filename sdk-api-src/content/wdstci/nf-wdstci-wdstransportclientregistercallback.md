---
UID: NF:wdstci.WdsTransportClientRegisterCallback
title: WdsTransportClientRegisterCallback function
author: windows-sdk-content
description: Registers a callback with the multicast client.
old-location: wds\wdstransportclientregistercallback.htm
old-project: wds
ms.assetid: e3c809c4-5681-4979-8633-bb8d3dbde35b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsTransportClientRegisterCallback, WdsTransportClientRegisterCallback function [Windows Deployment Services], wds.wdstransportclientregistercallback, wdstci/WdsTransportClientRegisterCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdstci.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRANSPORTCLIENT_CALLBACK_ID, *PTRANSPORTCLIENT_CALLBACK_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdstptc.dll
api_name:
 - WdsTransportClientRegisterCallback
product: Windows
targetos: Windows
req.lib: Wdstptc.lib
req.dll: Wdstptc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportClientRegisterCallback function


## -description


Registers a callback with the multicast client.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.


### -param CallbackId [in]

Identifier specifying which callback is being registered. This parameter receives a <a href="https://msdn.microsoft.com/6dd5e1ed-a9f8-4c6b-8bbb-8e3e6551d980">TRANSPORTCLIENT_CALLBACK_ID</a> enumeration value. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_SESSION_START</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="https://msdn.microsoft.com/47a053e3-f457-4d0a-80a8-1b93d5e8688f">PFN_WdsTransportClientSessionStart</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_RECEIVE_CONTENTS</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="https://msdn.microsoft.com/3a1cd9bb-c0da-4d66-9338-1f284fc15499">PFN_WdsTransportClientReceiveContents</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_SESSION_COMPLETE</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="https://msdn.microsoft.com/1c7b8137-bf74-486c-a90e-6becfec5ddc8">PFN_WdsTransportClientSessionComplete</a> callback. This callback is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WDS_TRANSPORTCLIENT_RECEIVE_METADATA</dt>
</dl>
</td>
<td width="60%">
Identifies the <a href="https://msdn.microsoft.com/9acde77b-5360-4c55-b11d-bf85e5c8d00e">PFN_WdsTransportClientReceiveMetadata</a> callback. This callback is optional.

</td>
</tr>
</table>
 


### -param pfnCallback [in]

Pointer to the function pointer associated with this id.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



All callbacks must be registered with the client before the consumer calls <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a>.  Once the session is started, no further callbacks may be registered. 



