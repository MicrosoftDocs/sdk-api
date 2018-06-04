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

# CALLINFO_BUFFER enumeration


## -description


The 
<b>CALLINFO_BUFFER</b> enum indicates the type of buffer accessed by the 
<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">ITCallInfo::GetCallInfoBuffer</a> method or the 
<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">ITCallInfo::SetCallInfoBuffer</a> method.

The 
<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">ITCallInfo::get_CallInfoBuffer</a> and 
<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">ITCallInfo::put_CallInfoBuffer</a> methods are provided for Automation client applications, such as those written in Visual Basic.


## -enum-fields




### -field CIB_USERUSERINFO

The user-user information buffer allows an application to send information to the remote party on a call or receive information from that party.


### -field CIB_DEVSPECIFICBUFFER

The device-specific buffer allows an application to communicate with a TSP concerning device-specific capabilities. The precise nature of these capabilities depends on the implementation of the service provider.


### -field CIB_CALLDATABUFFER

The call data buffer allows an application to communicate with a TSP concerning a specific call. The precise nature of this information depends on the implementation of the service provider.


### -field CIB_CHARGINGINFOBUFFER

The charging information buffer's format is specified by other standards (ISDN Q.931).


### -field CIB_HIGHLEVELCOMPATIBILITYBUFFER

The high-level compatibility buffer's format is specified by other standards (ISDN Q.931).


### -field CIB_LOWLEVELCOMPATIBILITYBUFFER

The low-level compatibility buffer's format is specified by other standards (ISDN Q.931).


## -see-also




<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">ITCallInfo::GetCallInfoBuffer</a>



<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">ITCallInfo::SetCallInfoBuffer</a>



<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">ITCallInfo::get_CallInfoBuffer</a>



<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">ITCallInfo::put_CallInfoBuffer</a>
 

 

