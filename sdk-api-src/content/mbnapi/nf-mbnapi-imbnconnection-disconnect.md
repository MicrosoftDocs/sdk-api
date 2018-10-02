---
UID: NF:mbnapi.IMbnConnection.Disconnect
title: IMbnConnection::Disconnect
author: windows-sdk-content
description: Disconnects a data connection.
old-location: mbn\imbnconnection_disconnect.htm
tech.root: mbn
ms.assetid: bc7f28db-499d-41be-a2cc-b4940a5bccd6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Disconnect, Disconnect method [Microsoft Broadband Networks], Disconnect method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],Disconnect method, IMbnConnection.Disconnect, IMbnConnection::Disconnect, mbn.imbnconnection_disconnect, mbnapi/IMbnConnection::Disconnect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnection.Disconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnection::Disconnect


## -description


Disconnects a data connection.


## -parameters




### -param requestID [out]

A pointer to a unique request ID assigned by the Mobile Broadband service to identify this asynchronous request.


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

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The connection has already been disconnected.

</td>
</tr>
</table>
 




## -remarks



Deactivation will also result in the disconnection of the L2 connection.

This is an asynchronous operation that will return immediately. If this method returns successfully, then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/2d225823-2b9b-4c3a-b847-7b2b9a13d121">OnDisconnectComplete</a> method of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a> when the operation is complete.

Windows 8 and later versions of Windows: A Windows Store app may only use <b>Disconnect</b> if the existing MBN connection was initiated by that app using <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">Connect</a>. <b>Disconnect</b> may not be used to disconnect connections that have been made by the user or by the <a href="https://msdn.microsoft.com/65f9fbc6-6b6c-4b73-996f-62c3f813911c">Windows Connection Manager</a>.




## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

