---
UID: NE:tapi3if.CALLINFO_BUFFER
title: CALLINFO_BUFFER
author: windows-sdk-content
description: The CALLINFO_BUFFER enum indicates the type of buffer accessed by the ITCallInfo::GetCallInfoBuffer method or the ITCallInfo::SetCallInfoBuffer method.
old-location: tapi3\callinfo_buffer.htm
old-project: tapi
ms.assetid: 76774741-2aa3-455c-a203-1daee42cf0fa
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CALLINFO_BUFFER, CALLINFO_BUFFER enumeration [TAPI 2.2], CIB_CALLDATABUFFER, CIB_CHARGINGINFOBUFFER, CIB_DEVSPECIFICBUFFER, CIB_HIGHLEVELCOMPATIBILITYBUFFER, CIB_LOWLEVELCOMPATIBILITYBUFFER, CIB_USERUSERINFO, _tapi3_callinfo_buffer, tapi3.callinfo_buffer, tapi3if/CALLINFO_BUFFER, tapi3if/CIB_CALLDATABUFFER, tapi3if/CIB_CHARGINGINFOBUFFER, tapi3if/CIB_DEVSPECIFICBUFFER, tapi3if/CIB_HIGHLEVELCOMPATIBILITYBUFFER, tapi3if/CIB_LOWLEVELCOMPATIBILITYBUFFER, tapi3if/CIB_USERUSERINFO
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CALLINFO_BUFFER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALLINFO_BUFFER
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

