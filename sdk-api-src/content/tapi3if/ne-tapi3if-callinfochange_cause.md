---
UID: NE:tapi3if.CALLINFOCHANGE_CAUSE
title: CALLINFOCHANGE_CAUSE
author: windows-sdk-content
description: The CALLINFOCHANGE_CAUSE enum is used by the ITCallInfoChangeEvent::get_Cause method to return a description of the type of call information that has changed.
old-location: tapi3\callinfochange_cause.htm
old-project: tapi
ms.assetid: 587329e2-3b5f-4d9e-9cec-2676c0bd1de8
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CALLINFOCHANGE_CAUSE, CALLINFOCHANGE_CAUSE enumeration [TAPI 2.2], CIC_APPSPECIFIC, CIC_BEARERMODE, CIC_CALLDATA, CIC_CALLEDID, CIC_CALLERID, CIC_CALLID, CIC_CHARGINGINFO, CIC_COMPLETIONID, CIC_CONNECTEDID, CIC_DEVSPECIFIC, CIC_HIGHLEVELCOMP, CIC_LOWLEVELCOMP, CIC_MEDIATYPE, CIC_NUMMONITORS, CIC_NUMOWNERDECR, CIC_NUMOWNERINCR, CIC_ORIGIN, CIC_OTHER, CIC_PRIVILEGE, CIC_RATE, CIC_REASON, CIC_REDIRECTINGID, CIC_REDIRECTIONID, CIC_RELATEDCALLID, CIC_TREATMENT, CIC_TRUNK, CIC_USERUSERINFO, _tapi3_callinfochange_cause, tapi3.callinfochange_cause, tapi3if/CALLINFOCHANGE_CAUSE, tapi3if/CIC_APPSPECIFIC, tapi3if/CIC_BEARERMODE, tapi3if/CIC_CALLDATA, tapi3if/CIC_CALLEDID, tapi3if/CIC_CALLERID, tapi3if/CIC_CALLID, tapi3if/CIC_CHARGINGINFO, tapi3if/CIC_COMPLETIONID, tapi3if/CIC_CONNECTEDID, tapi3if/CIC_DEVSPECIFIC, tapi3if/CIC_HIGHLEVELCOMP, tapi3if/CIC_LOWLEVELCOMP, tapi3if/CIC_MEDIATYPE, tapi3if/CIC_NUMMONITORS, tapi3if/CIC_NUMOWNERDECR, tapi3if/CIC_NUMOWNERINCR, tapi3if/CIC_ORIGIN, tapi3if/CIC_OTHER, tapi3if/CIC_PRIVILEGE, tapi3if/CIC_RATE, tapi3if/CIC_REASON, tapi3if/CIC_REDIRECTINGID, tapi3if/CIC_REDIRECTIONID, tapi3if/CIC_RELATEDCALLID, tapi3if/CIC_TREATMENT, tapi3if/CIC_TRUNK, tapi3if/CIC_USERUSERINFO
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
req.typenames: CALLINFOCHANGE_CAUSE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALLINFOCHANGE_CAUSE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

