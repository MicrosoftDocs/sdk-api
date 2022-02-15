---
UID: NE:tapi3if.CALLINFOCHANGE_CAUSE
title: CALLINFOCHANGE_CAUSE (tapi3if.h)
description: The CALLINFOCHANGE_CAUSE enum is used by the ITCallInfoChangeEvent::get_Cause method to return a description of the type of call information that has changed.
helpviewer_keywords: ["CALLINFOCHANGE_CAUSE","CALLINFOCHANGE_CAUSE enumeration [TAPI 2.2]","CIC_APPSPECIFIC","CIC_BEARERMODE","CIC_CALLDATA","CIC_CALLEDID","CIC_CALLERID","CIC_CALLID","CIC_CHARGINGINFO","CIC_COMPLETIONID","CIC_CONNECTEDID","CIC_DEVSPECIFIC","CIC_HIGHLEVELCOMP","CIC_LOWLEVELCOMP","CIC_MEDIATYPE","CIC_NUMMONITORS","CIC_NUMOWNERDECR","CIC_NUMOWNERINCR","CIC_ORIGIN","CIC_OTHER","CIC_PRIVILEGE","CIC_RATE","CIC_REASON","CIC_REDIRECTINGID","CIC_REDIRECTIONID","CIC_RELATEDCALLID","CIC_TREATMENT","CIC_TRUNK","CIC_USERUSERINFO","_tapi3_callinfochange_cause","tapi3.callinfochange_cause","tapi3if/CALLINFOCHANGE_CAUSE","tapi3if/CIC_APPSPECIFIC","tapi3if/CIC_BEARERMODE","tapi3if/CIC_CALLDATA","tapi3if/CIC_CALLEDID","tapi3if/CIC_CALLERID","tapi3if/CIC_CALLID","tapi3if/CIC_CHARGINGINFO","tapi3if/CIC_COMPLETIONID","tapi3if/CIC_CONNECTEDID","tapi3if/CIC_DEVSPECIFIC","tapi3if/CIC_HIGHLEVELCOMP","tapi3if/CIC_LOWLEVELCOMP","tapi3if/CIC_MEDIATYPE","tapi3if/CIC_NUMMONITORS","tapi3if/CIC_NUMOWNERDECR","tapi3if/CIC_NUMOWNERINCR","tapi3if/CIC_ORIGIN","tapi3if/CIC_OTHER","tapi3if/CIC_PRIVILEGE","tapi3if/CIC_RATE","tapi3if/CIC_REASON","tapi3if/CIC_REDIRECTINGID","tapi3if/CIC_REDIRECTIONID","tapi3if/CIC_RELATEDCALLID","tapi3if/CIC_TREATMENT","tapi3if/CIC_TRUNK","tapi3if/CIC_USERUSERINFO"]
old-location: tapi3\callinfochange_cause.htm
tech.root: tapi3
ms.assetid: 587329e2-3b5f-4d9e-9cec-2676c0bd1de8
ms.date: 12/05/2018
ms.keywords: CALLINFOCHANGE_CAUSE, CALLINFOCHANGE_CAUSE enumeration [TAPI 2.2], CIC_APPSPECIFIC, CIC_BEARERMODE, CIC_CALLDATA, CIC_CALLEDID, CIC_CALLERID, CIC_CALLID, CIC_CHARGINGINFO, CIC_COMPLETIONID, CIC_CONNECTEDID, CIC_DEVSPECIFIC, CIC_HIGHLEVELCOMP, CIC_LOWLEVELCOMP, CIC_MEDIATYPE, CIC_NUMMONITORS, CIC_NUMOWNERDECR, CIC_NUMOWNERINCR, CIC_ORIGIN, CIC_OTHER, CIC_PRIVILEGE, CIC_RATE, CIC_REASON, CIC_REDIRECTINGID, CIC_REDIRECTIONID, CIC_RELATEDCALLID, CIC_TREATMENT, CIC_TRUNK, CIC_USERUSERINFO, _tapi3_callinfochange_cause, tapi3.callinfochange_cause, tapi3if/CALLINFOCHANGE_CAUSE, tapi3if/CIC_APPSPECIFIC, tapi3if/CIC_BEARERMODE, tapi3if/CIC_CALLDATA, tapi3if/CIC_CALLEDID, tapi3if/CIC_CALLERID, tapi3if/CIC_CALLID, tapi3if/CIC_CHARGINGINFO, tapi3if/CIC_COMPLETIONID, tapi3if/CIC_CONNECTEDID, tapi3if/CIC_DEVSPECIFIC, tapi3if/CIC_HIGHLEVELCOMP, tapi3if/CIC_LOWLEVELCOMP, tapi3if/CIC_MEDIATYPE, tapi3if/CIC_NUMMONITORS, tapi3if/CIC_NUMOWNERDECR, tapi3if/CIC_NUMOWNERINCR, tapi3if/CIC_ORIGIN, tapi3if/CIC_OTHER, tapi3if/CIC_PRIVILEGE, tapi3if/CIC_RATE, tapi3if/CIC_REASON, tapi3if/CIC_REDIRECTINGID, tapi3if/CIC_REDIRECTIONID, tapi3if/CIC_RELATEDCALLID, tapi3if/CIC_TREATMENT, tapi3if/CIC_TRUNK, tapi3if/CIC_USERUSERINFO
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
targetos: Windows
req.typenames: CALLINFOCHANGE_CAUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLINFOCHANGE_CAUSE
 - tapi3if/CALLINFOCHANGE_CAUSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALLINFOCHANGE_CAUSE
---

# CALLINFOCHANGE_CAUSE enumeration


## -description

The 
<b>CALLINFOCHANGE_CAUSE</b> enum is used by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause">ITCallInfoChangeEvent::get_Cause</a> method to return a description of the type of call information that has changed.

You can retrieve specific information about the change by using the TAPI 3 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface. TAPI 2 applications use 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallstatus">lineGetCallStatus</a>.

## -enum-fields

### -field CIC_OTHER:0

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

<a href="/windows/desktop/Tapi/linecallprivilege--constants">Call privilege</a> has changed.

### -field CIC_MEDIATYPE

The call 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> has changed.

### -field CIC_LASTITEM

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause">ITCallInfoChangeEvent::get_Cause</a>
