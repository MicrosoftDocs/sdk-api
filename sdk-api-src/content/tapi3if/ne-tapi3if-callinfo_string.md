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

# CALLINFO_STRING enumeration


## -description


The 
<b>CALLINFO_STRING</b> enum is used by 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> methods that set and get call information involving the use of strings.


## -enum-fields




### -field CIS_CALLERIDNAME

The name of the caller.


### -field CIS_CALLERIDNUMBER

The number of the caller.


### -field CIS_CALLEDIDNAME

The name of the called location.


### -field CIS_CALLEDIDNUMBER

The number of the called location.


### -field CIS_CONNECTEDIDNAME

The name of the connected location.


### -field CIS_CONNECTEDIDNUMBER

The number of the connected location.


### -field CIS_REDIRECTIONIDNAME

The name of the location to which a call has been redirected.


### -field CIS_REDIRECTIONIDNUMBER

The number of the location to which a call has been redirected.


### -field CIS_REDIRECTINGIDNAME

The name of the location that redirected the call.


### -field CIS_REDIRECTINGIDNUMBER

The number of the location that redirected the call.


### -field CIS_CALLEDPARTYFRIENDLYNAME

The called party friendly name.


### -field CIS_COMMENT

A comment about the call provided by the application that originated the call. The call state must be CS_IDLE when setting the comment.


### -field CIS_DISPLAYABLEADDRESS

A displayable version of the called or calling address.


### -field CIS_CALLINGPARTYID

The identifier of the calling party.


## -see-also




<a href="https://msdn.microsoft.com/248022e7-c6cf-4c46-be94-ee1b79b9f39a">ITCallInfo::get_CallInfoString</a>



<a href="https://msdn.microsoft.com/d22f1afb-e036-40d0-9a7f-61d8d24d2376">ITCallInfo::put_CallInfoString</a>
 

 

