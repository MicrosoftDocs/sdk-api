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

# QOS_EVENT enumeration


## -description


The 
<b>QOS_EVENT</b> enum describes quality of service (QOS) events. The 
<a href="https://msdn.microsoft.com/8e0f4705-6614-4973-85bd-21abd17bd7fe">ITQOSEvent::get_Event</a> method returns a member of this enum to indicate the type of QOS event that occurred.


## -enum-fields




### -field QE_NOQOS

QOS is not available.


### -field QE_ADMISSIONFAILURE

The QOS request could not be met.


### -field QE_POLICYFAILURE

The type of QOS requested is not supported.


### -field QE_GENERICERROR

Unspecified QOS error.


### -field QE_LASTITEM




## -see-also




<a href="https://msdn.microsoft.com/f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd">ITBasicCallControl::SetQOS</a>



<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>



<a href="https://msdn.microsoft.com/8e0f4705-6614-4973-85bd-21abd17bd7fe">ITQOSEvent::get_Event</a>



<a href="https://msdn.microsoft.com/8b0a93ab-6445-4c60-9d27-552c355c1355">QOS_SERVICE_LEVEL</a>
 

 

