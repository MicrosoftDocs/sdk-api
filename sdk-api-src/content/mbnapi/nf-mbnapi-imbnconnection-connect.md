---
UID: NF:mbnapi.IMbnConnection.Connect
title: IMbnConnection::Connect
author: windows-sdk-content
description: Establishes a data connection.
old-location: mbn\imbnconnection_connect.htm
old-project: mbn
ms.assetid: 66acb84e-8e0f-4ff1-abc4-b32f782ce9f3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Connect, Connect method [Microsoft Broadband Networks], Connect method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],Connect method, IMbnConnection.Connect, IMbnConnection::Connect, mbn.imbnconnection_connect, mbnapi/IMbnConnection::Connect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnConnection.Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnection::Connect


## -description


Establishes a data connection.


## -parameters




### -param connectionMode [in]

An <a href="https://msdn.microsoft.com/c7aed29b-7938-4266-ae4c-b8ba84eb8a63">MBN_CONNECTION_MODE</a> value that specifies the mode of the connection.


### -param strProfile [in]

Contains the profile designator.


### -param requestID [out]

A pointer to a unique request ID returned by the Mobile Broadband service to identify this asynchronous request.


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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid profile name was specified or the <i>strProfile</i> argument is not compliant to XML profile schema

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_MAX_ACTIVATED_CONTEXTS</b></dt>
</dl>
</td>
<td width="60%">
There is already an active Mobile Broadband context.  Multiple active contexts are not supported.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">Connect</a> method is used to activate a connection context for the device. The Mobile Broadband service currently supports at most one active context. Activation of the context will also result in L2 connection also being established. Similarly, deactivation of a context will result in disconnection of the physical data connection to the mobile network.

If the device is not in the packet-attached state at the time of calling this operation then the Mobile Broadband service will implicitly packet attach the device before issuing the connect request to the device. If there is any packet service state change then application will be notified by a call to the <a href="https://msdn.microsoft.com/19199009-a4ac-4bf9-adfc-46c06d861485">OnPacketServiceStateChange</a> method of the <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a> interface.

If <i>connectionMode</i> is set to <b>MBN_CONNECTION_MODE_PROFILE</b>, then <i>strProfile</i> represents the name of the profile for the device. If set to <b>MBN_CONNECTION_MODE_TMP_PROFILE</b>, then <i>strProfile</i> represents the XML representation of the profile. A calling application can use <a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a> to get a list of connection profiles stored in the device.


This is an asynchronous operation that will return immediately. If this method returns successfully, then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/d770eda5-43f4-44d3-a870-fc54f9374610">OnConnectComplete</a> method of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a> when the operation is complete.


Windows 8 and later versions of Windows: A Windows Store app may use <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">Connect</a> with only the  <a href="https://msdn.microsoft.com/c7aed29b-7938-4266-ae4c-b8ba84eb8a63">MBN_CONNECTION_MODE_TMP_PROFILE</a><i>connectionMode</i> and the <i>strProfile</i> parameter set to an XML representation of the profile. This implies that the connection is of a temporary nature and not saved for future use by the system.




## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

