---
UID: NE:tapi3if.CALLINFO_LONG
title: CALLINFO_LONG
author: windows-sdk-content
description: The CALLINFO_LONG enum is used by ITCallInfo methods that set and get call information of type LONG.
old-location: tapi3\callinfo_long.htm
old-project: tapi
ms.assetid: 48a27ba2-e21d-46bb-8fba-8052fc68b851
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CALLINFO_LONG, CALLINFO_LONG enumeration [TAPI 2.2], CIL_APPSPECIFIC, CIL_BEARERMODE, CIL_CALLEDIDADDRESSTYPE, CIL_CALLERIDADDRESSTYPE, CIL_CALLID, CIL_CALLPARAMSFLAGS, CIL_CALLTREATMENT, CIL_COMPLETIONID, CIL_CONNECTEDIDADDRESSTYPE, CIL_COUNTRYCODE, CIL_MAXRATE, CIL_MEDIATYPESAVAILABLE, CIL_MINRATE, CIL_NUMBEROFMONITORS, CIL_NUMBEROFOWNERS, CIL_ORIGIN, CIL_RATE, CIL_REASON, CIL_REDIRECTINGIDADDRESSTYPE, CIL_REDIRECTIONIDADDRESSTYPE, CIL_RELATEDCALLID, CIL_TRUNK, _tapi3_callinfo_long, tapi3.callinfo_long, tapi3if/CALLINFO_LONG, tapi3if/CIL_APPSPECIFIC, tapi3if/CIL_BEARERMODE, tapi3if/CIL_CALLEDIDADDRESSTYPE, tapi3if/CIL_CALLERIDADDRESSTYPE, tapi3if/CIL_CALLID, tapi3if/CIL_CALLPARAMSFLAGS, tapi3if/CIL_CALLTREATMENT, tapi3if/CIL_COMPLETIONID, tapi3if/CIL_CONNECTEDIDADDRESSTYPE, tapi3if/CIL_COUNTRYCODE, tapi3if/CIL_MAXRATE, tapi3if/CIL_MEDIATYPESAVAILABLE, tapi3if/CIL_MINRATE, tapi3if/CIL_NUMBEROFMONITORS, tapi3if/CIL_NUMBEROFOWNERS, tapi3if/CIL_ORIGIN, tapi3if/CIL_RATE, tapi3if/CIL_REASON, tapi3if/CIL_REDIRECTINGIDADDRESSTYPE, tapi3if/CIL_REDIRECTIONIDADDRESSTYPE, tapi3if/CIL_RELATEDCALLID, tapi3if/CIL_TRUNK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.redist: 
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
req.typenames: CALLINFO_LONG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALLINFO_LONG
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CALLINFO_LONG enumeration


## -description


The 
<b>CALLINFO_LONG</b> enum is used by 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> methods that set and get call information of type <b>LONG</b>.


## -enum-fields




### -field CIL_MEDIATYPESAVAILABLE

The 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> available on the call.


### -field CIL_BEARERMODE

The bearer mode of a call is described by the 
<a href="https://msdn.microsoft.com/87e46ec9-ed5f-4ff5-a382-34eb164f4e66">LINEBEARERMODE_ Constants</a>.


### -field CIL_CALLERIDADDRESSTYPE

The 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> of the caller.


### -field CIL_CALLEDIDADDRESSTYPE

The 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> of the called party.


### -field CIL_CONNECTEDIDADDRESSTYPE

The 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> of the connected party.


### -field CIL_REDIRECTIONIDADDRESSTYPE

The 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> of the destination to which a call has been redirected.


### -field CIL_REDIRECTINGIDADDRESSTYPE

The 
<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">address type</a> of the location that redirected the call.


### -field CIL_ORIGIN

The origin of a call is described by the 
<a href="https://msdn.microsoft.com/b830a40e-62d9-4a6c-b43f-8318f30a7cd4">LINECALLORIGIN_ Constants</a>, such as LINECALLORIGIN_EXTERNAL.


### -field CIL_REASON

The reason for a call is described by the 
<a href="https://msdn.microsoft.com/16278146-886f-433a-afe5-64f4894b1428">LINECALLREASON_ Constants</a>, such as LINECALLREASON_FWDUNCOND.


### -field CIL_APPSPECIFIC

Application-specific information is used to pass information between applications in a multi-application environment. The information is not interpreted by the API implementation or the service provider. Only applications with owner privileges for the call can set it.


### -field CIL_CALLPARAMSFLAGS

Call parameter flags are described by 
<a href="https://msdn.microsoft.com/f323ec9f-5bab-4b5d-93ef-8a552ee0d591">LINECALLPARAMFLAGS_ Constants</a>, such as LINECALLPARAMFLAGS_BLOCKID. These flags are normally set during the creation of an outgoing call.


### -field CIL_CALLTREATMENT

Call treatment identifies how a call that is on hold or unanswered gets handled, and is described by 
<a href="https://msdn.microsoft.com/c28c9200-dd51-48b2-905c-fbe37c83b00f">LINECALLTREATMENT_ Constants</a>, such as LINECALLTREATMENT_MUSIC.


### -field CIL_MINRATE

The minimum rate for a call's data stream in bps (bits per second).


### -field CIL_MAXRATE

The maximum rate for a call's data stream in bps (bits per second).


### -field CIL_COUNTRYCODE

Country or region code.


### -field CIL_CALLID

Call identifier. Some service providers assign a unique code to each call.


### -field CIL_RELATEDCALLID

Call identifier for a call related to the current call, such as on a conference.


### -field CIL_COMPLETIONID

Completion identifier. The completion identifier is used to identify individual completion requests in progress. A completion identifier becomes invalid and can be reused after the request completion or after an outstanding request is canceled.


### -field CIL_NUMBEROFOWNERS

The number of applications having owner privileges for the current call.


### -field CIL_NUMBEROFMONITORS

The number of applications having monitor privileges for the current call.


### -field CIL_TRUNK

The trunk identifier for the current call.


### -field CIL_RATE

The current rate for a call's data stream in bps (bits per second).


### -field CIL_GENERATEDIGITDURATION


### -field CIL_MONITORDIGITMODES


### -field CIL_MONITORMEDIAMODES




## -see-also




<a href="https://msdn.microsoft.com/0c00e672-7bad-4a44-a76a-efd222f763d7">ITCallInfo::get_CallInfoLong</a>



<a href="https://msdn.microsoft.com/b5198b78-56f7-4964-970a-1068f2db4743">ITCallInfo::put_CallInfoLong</a>
 

 

