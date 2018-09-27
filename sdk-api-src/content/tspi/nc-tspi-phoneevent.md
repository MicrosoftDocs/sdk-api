---
UID: NC:tspi.PHONEEVENT
title: PHONEEVENT
author: windows-sdk-content
description: Phone_Event a callback function implemented by TAPI and supplied to the service provider as a parameter to TSPI_phoneOpen. The service provider calls this function to report events that occur on the phone.
old-location: tspi\phone_event_tspi.htm
tech.root: tapi
ms.assetid: 0b5745a4-7652-48ce-9e8a-eef52c09455f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: PHONEEVENT, PHONEEVENT callback, Phone_Event, Phone_Event callback function [TAPI 2.2], _tspi_phoneevent, tspi.phone_event_tspi, tspi.phoneevent, tspi/Phone_Event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: tspi.h
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
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - Phone_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PHONEEVENT callback function


## -description


<i>Phone_Event</i> a callback function implemented by TAPI and supplied to the service provider as a parameter to 
<a href="https://msdn.microsoft.com/e2a4372f-62ff-488c-94a7-ed44388b8092">TSPI_phoneOpen</a>. The service provider calls this function to report events that occur on the phone.

The <b>PHONEEVENT</b> type defines a pointer to this callback function. <i>Phone_Event</i> is a placeholder for the application-defined function name.


## -parameters




### -param htPhone

The TAPI handle for the phone on which the event occurred.


### -param dwMsg

Specifies the kind of event that is being reported. Interpretation of the other parameters is done in different ways according to the context indicated by <i>dwMsg</i>.


### -param dwParam1

A parameter for the message.


### -param dwParam2

A parameter for the message.


### -param dwParam3

A parameter for the message.


## -returns



This function has no return value.




## -remarks



The call state when calling this function can be any state.

The service provider passes the 
<a href="https://msdn.microsoft.com/e869cb3e-0eeb-4edf-a272-a655a236a3a2">HTAPIPHONE</a> value supplied to 
<a href="https://msdn.microsoft.com/e2a4372f-62ff-488c-94a7-ed44388b8092">TSPI_phoneOpen</a> as the <i>htPhone</i> parameter. It includes the message identifier and parameters specific to the event.

The sets of messages that can be passed to this procedure differ slightly from the messages to the corresponding callback at the TAPI level. In particular, completion of asynchronously executing requests is reported through the 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">Completion_Proc</a> callback instead of this one.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">Completion_Proc</a>



<a href="https://msdn.microsoft.com/97cde843-65bc-46ae-a6ae-724f2c9c5217">TSPI_lineOpen</a>
 

 

