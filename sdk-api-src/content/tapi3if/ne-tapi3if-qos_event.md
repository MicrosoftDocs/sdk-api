---
UID: NE:tapi3if.QOS_EVENT
title: QOS_EVENT (tapi3if.h)
author: windows-sdk-content
description: The QOS_EVENT enum describes quality of service (QOS) events. The ITQOSEvent::get_Event method returns a member of this enum to indicate the type of QOS event that occurred.
old-location: tapi3\qos_event.htm
tech.root: Tapi
ms.assetid: 8bf4bfdc-6327-497d-9d19-4771d47982bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QE_ADMISSIONFAILURE, QE_GENERICERROR, QE_NOQOS, QE_POLICYFAILURE, QOS_EVENT, QOS_EVENT enumeration [TAPI 2.2], _tapi3_qos_event, tapi3.qos_event, tapi3if/QE_ADMISSIONFAILURE, tapi3if/QE_GENERICERROR, tapi3if/QE_NOQOS, tapi3if/QE_POLICYFAILURE, tapi3if/QOS_EVENT
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - QOS_EVENT
product: Windows
targetos: Windows
req.typenames: QOS_EVENT
req.redist: 
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
 

 

