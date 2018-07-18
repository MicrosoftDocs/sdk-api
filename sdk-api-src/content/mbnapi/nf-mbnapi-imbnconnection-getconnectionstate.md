---
UID: NF:mbnapi.IMbnConnection.GetConnectionState
title: IMbnConnection::GetConnectionState
author: windows-sdk-content
description: Gets the current connection state of the device.
old-location: mbn\imbnconnection_getconnectionstate.htm
old-project: mbn
ms.assetid: 85f3e0bb-c694-4870-b423-cb4ac7a0477d
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetConnectionState, GetConnectionState method [Microsoft Broadband Networks], GetConnectionState method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],GetConnectionState method, IMbnConnection.GetConnectionState, IMbnConnection::GetConnectionState, mbn.imbnconnection_getconnectionstate, mbnapi/IMbnConnection::GetConnectionState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnection.GetConnectionState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnection::GetConnectionState


## -description


Gets the current connection state of the device.


## -parameters




### -param ConnectionState [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/712b9ead-8e38-45b1-8dff-b8906056d3d6">MBN_ACTIVATION_STATE</a> structure  that contains the state of the connection.


### -param ProfileName [out, retval]

A pointer to a string that contains the name of the connection profile.  This parameter is valid only when <i>ConnectionState</i> is <b>MBN_ACTIVATION_STATE_ACTIVATED</b>.  When this string is not <b>NULL</b>, the calling application must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


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
The method completed successfully.

<div class="alert"><b>Note</b>  This method can return S_OK when <i>ProfileName</i> is <b>NULL</b>. Make sure that your client is capable of handling a <b>NULL</b> <i>ProfileName</i> even if the call is successful.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The activation state not available.  The Mobile Broadband service is probing the device for the information.  The calling application can be notified when the activation state is available by registering for the <a href="https://msdn.microsoft.com/5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8">OnConnectStateChange</a> method of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the call state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>
 




## -remarks



This method can return S_OK when <i>ProfileName</i> is <b>NULL</b>. Make sure that your client is capable of handling a <b>NULL</b><i>ProfileName</i> even if the call is successful.




## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

