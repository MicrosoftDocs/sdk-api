---
UID: NF:tapi3if.ITBasicCallControl.Disconnect
title: ITBasicCallControl::Disconnect
author: windows-sdk-content
description: The Disconnect method disconnects the call. The call state will transition to CS_DISCONNECTED after the method completes successfully.
old-location: tapi3\itbasiccallcontrol_disconnect.htm
old-project: tapi
ms.assetid: b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: Disconnect, Disconnect method [TAPI 2.2], Disconnect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Disconnect method, ITBasicCallControl.Disconnect, ITBasicCallControl::Disconnect, _tapi3_itbasiccallcontrol_disconnect, tapi3.itbasiccallcontrol_disconnect, tapi3if/ITBasicCallControl::Disconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.Disconnect
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl::Disconnect


## -description


The 
<b>Disconnect</b> method disconnects the call. The 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> will transition to CS_DISCONNECTED after the method completes successfully.


## -parameters




### -param code [in]


<a href="https://msdn.microsoft.com/90e7b63f-3e19-422d-b45b-43408de9c6cc">DISCONNECT_CODE</a> indicating reason for call disconnection.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The call state is CS_IDLE or a valid handle for the call could not be obtained by the TAPI 3 DLL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/90e7b63f-3e19-422d-b45b-43408de9c6cc">DISCONNECT_CODE</a>



<a href="https://msdn.microsoft.com/dc348bb2-d564-40f8-afe3-5473c5769fa4">Drop overview</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d">Terminate a Session Overview</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>
 

 

