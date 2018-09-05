---
UID: NF:mbnapi.IMbnInterface.GetReadyState
title: IMbnInterface::GetReadyState
author: windows-sdk-content
description: Gets the ready state.
old-location: mbn\imbninterface_getreadystate.htm
old-project: mbn
ms.assetid: 4236fd9d-292a-4840-b52e-c28c3e6eea10
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetReadyState, GetReadyState method [Microsoft Broadband Networks], GetReadyState method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetReadyState method, IMbnInterface.GetReadyState, IMbnInterface::GetReadyState, mbn.imbninterface_getreadystate, mbnapi/IMbnInterface::GetReadyState
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
 - IMbnInterface.GetReadyState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterface::GetReadyState


## -description


Gets the ready state.


## -parameters




### -param readyState [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/4f712cdc-ee9c-4ceb-9bc4-8a4fe19d0a37">MBN_READY_STATE</a> structure.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.


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
The method completed successfully.  <i>readyState</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for the ready state.  The calling application can get notified when the ready state is available by registering for the <a href="https://msdn.microsoft.com/eb4364b8-cbbf-44c7-ae13-66950ce614e9">OnReadyStateChange</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>
 




## -remarks



The ready state specifies whether the interface is successfully initialized and is ready to perform connection operations. For SIM-based devices, a device is ready when the SIM has been initialized successfully by the device. The device can be used for connection only when the ready state is <b>MBN_READY_STATE_INITIALIZED</b>. For more information about other device states, see <a href="https://msdn.microsoft.com/4f712cdc-ee9c-4ceb-9bc4-8a4fe19d0a37">MBN_READY_STATE</a>.

The ready state of an interface can change as a result of a user operation. For example, when a user inserts a SIM into a device, the ready state changes from <b>MBN_READY_STATE_SIM_NOT_INSERTED</b> to another ready state. The ready state can also change because of other operations performed by the application. For example, when a PIN has been entered, the ready state can change from <b>MBN_READY_STATE_DEVICE_LOCKED</b> to another ready state. An application can register for event notifications whenever there is a change in the ready state of the interface. The <a href="https://msdn.microsoft.com/eb4364b8-cbbf-44c7-ae13-66950ce614e9">OnReadyStateChange</a> member of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a> is called to notify an application about any change in the ready state.

The device's SMS subsystem may not be ready when it reports <b>MBN_READY_STATE_INITIALIZED</b>.   A calling application should wait for  a call to the <a href="https://msdn.microsoft.com/d6990732-60ef-43e5-b35c-9a3f0324d580">OnSmsConfigurationChange</a> member of <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>, indicating that the SMS subsystem is ready.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 

