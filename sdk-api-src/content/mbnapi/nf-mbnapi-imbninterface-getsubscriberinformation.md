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

# IMbnInterface::GetSubscriberInformation


## -description


Gets the subscriber information.


## -parameters




### -param subscriberInformation [out, retval]

A pointer to the address of an <a href="https://msdn.microsoft.com/ef7f5dc5-ed66-450c-9623-0c1d725d82c6">IMbnSubscriberInformation</a> interface that contains subscriber information for the device.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.


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
The method completed successfully.  <i>subscriberInformation</i> contains a valid interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for the information.  The calling application can get notified when the information is available by registering for the <a href="https://msdn.microsoft.com/26d4fbdb-9c13-4934-a6bb-df581d0c18e9">OnSubscriberInformationChange</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>GetSubscriberInformation</b> method returns the subscriber-related information, including subscriber ID, SIM international circuit card number, and phone numbers associated with this interface.

When this method is called from a Windows Store app with mobile operator privileges  it will only return the SIM International circuit card number defined by   the <a href="https://msdn.microsoft.com/18132836-65e8-4372-bfcd-ba0115b2d4d0">SimIccID</a> property.

Some of the values returned in subscriber information are populated only when the ready state which as reported by the <a href="https://msdn.microsoft.com/4236fd9d-292a-4840-b52e-c28c3e6eea10">GetReadyState</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> is <b>MBN_READY_STATE_INITIALIZED</b>. Whenever there is a change in the subscriber information associated with the Mobile Broadband device, the Mobile Broadband service will notify registered applications by calling the <a href="https://msdn.microsoft.com/26d4fbdb-9c13-4934-a6bb-df581d0c18e9">OnSubscriberInformationChange</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

Subscriber information for a device will not change once the device ready state is <b>MBN_READY_STATE_INITIALIZED</b>.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 

