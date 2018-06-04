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

# CALLINFOCHANGE_CAUSE enumeration


## -description


The 
<b>CALLINFOCHANGE_CAUSE</b> enum is used by the 
<a href="https://msdn.microsoft.com/c49a5624-8867-46c0-acf6-5e60667fc969">ITCallInfoChangeEvent::get_Cause</a> method to return a description of the type of call information that has changed.

You can retrieve specific information about the change by using the TAPI 3 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface. TAPI 2 applications use 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a> or 
<a href="https://msdn.microsoft.com/88bcd211-0993-4703-b43f-4e0b93e3eb7e">lineGetCallStatus</a>.


## -enum-fields




### -field CIC_OTHER

Unspecified call information has changed.


### -field CIC_DEVSPECIFIC

Call information specific to a device has changed.


### -field CIC_BEARERMODE

The bearer mode for the call has changed.


### -field CIC_RATE

The rate has changed.


### -field CIC_APPSPECIFIC

Call information specific to an application has changed. Application-specific information is used to pass information between applications in a multi-application environment. The information is not interpreted by the API implementation or the service provider. Only applications with owner privileges for the call can set it


### -field CIC_CALLID

The call identifier has changed.


### -field CIC_RELATEDCALLID

The related call identifier has changed.


### -field CIC_ORIGIN

The call origin has changed.


### -field CIC_REASON

The call reason has changed.


### -field CIC_COMPLETIONID

The completion identifier has changed.


### -field CIC_NUMOWNERINCR

The number of owners has increased.


### -field CIC_NUMOWNERDECR

The number of owners has decreased.


### -field CIC_NUMMONITORS

The number of call monitors has changed.


### -field CIC_TRUNK

Trunk used on call has changed.


### -field CIC_CALLERID

The caller identifier has changed.


### -field CIC_CALLEDID

The called identifier has changed.


### -field CIC_CONNECTEDID

The connected identifier has changed.


### -field CIC_REDIRECTIONID

The redirection identifier has changed.


### -field CIC_REDIRECTINGID

The redirecting identifier has changed.


### -field CIC_USERUSERINFO

The user-user information buffer has changed.


### -field CIC_HIGHLEVELCOMP

The high-level compatibility information has changed (ISDN Q.931).


### -field CIC_LOWLEVELCOMP

The low-level compatibility information has changed (ISDN Q.931).


### -field CIC_CHARGINGINFO

The call's charging information has changed.


### -field CIC_TREATMENT

Treatment of calls on hold has changed.


### -field CIC_CALLDATA

The call data buffer has changed.


### -field CIC_PRIVILEGE


<a href="https://msdn.microsoft.com/a58b7e9e-696e-4421-9b31-1ba8afe6e03b">Call privilege</a> has changed.


### -field CIC_MEDIATYPE

The call 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> has changed.


### -field CIC_LASTITEM




## -see-also




<a href="https://msdn.microsoft.com/c49a5624-8867-46c0-acf6-5e60667fc969">ITCallInfoChangeEvent::get_Cause</a>
 

 

