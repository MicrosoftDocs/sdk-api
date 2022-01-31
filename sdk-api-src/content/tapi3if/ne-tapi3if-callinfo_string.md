---
UID: NE:tapi3if.CALLINFO_STRING
title: CALLINFO_STRING (tapi3if.h)
description: The CALLINFO_STRING enum is used by ITCallInfo methods that set and get call information involving the use of strings.
helpviewer_keywords: ["CALLINFO_STRING","CALLINFO_STRING enumeration [TAPI 2.2]","CIS_CALLEDIDNAME","CIS_CALLEDIDNUMBER","CIS_CALLEDPARTYFRIENDLYNAME","CIS_CALLERIDNAME","CIS_CALLERIDNUMBER","CIS_CALLINGPARTYID","CIS_COMMENT","CIS_CONNECTEDIDNAME","CIS_CONNECTEDIDNUMBER","CIS_DISPLAYABLEADDRESS","CIS_REDIRECTINGIDNAME","CIS_REDIRECTINGIDNUMBER","CIS_REDIRECTIONIDNAME","CIS_REDIRECTIONIDNUMBER","_tapi3_callinfo_string","tapi3.callinfo_string","tapi3if/CALLINFO_STRING","tapi3if/CIS_CALLEDIDNAME","tapi3if/CIS_CALLEDIDNUMBER","tapi3if/CIS_CALLEDPARTYFRIENDLYNAME","tapi3if/CIS_CALLERIDNAME","tapi3if/CIS_CALLERIDNUMBER","tapi3if/CIS_CALLINGPARTYID","tapi3if/CIS_COMMENT","tapi3if/CIS_CONNECTEDIDNAME","tapi3if/CIS_CONNECTEDIDNUMBER","tapi3if/CIS_DISPLAYABLEADDRESS","tapi3if/CIS_REDIRECTINGIDNAME","tapi3if/CIS_REDIRECTINGIDNUMBER","tapi3if/CIS_REDIRECTIONIDNAME","tapi3if/CIS_REDIRECTIONIDNUMBER"]
old-location: tapi3\callinfo_string.htm
tech.root: tapi3
ms.assetid: 28482ba8-c536-48ef-bca6-eba5b801c06e
ms.date: 12/05/2018
ms.keywords: CALLINFO_STRING, CALLINFO_STRING enumeration [TAPI 2.2], CIS_CALLEDIDNAME, CIS_CALLEDIDNUMBER, CIS_CALLEDPARTYFRIENDLYNAME, CIS_CALLERIDNAME, CIS_CALLERIDNUMBER, CIS_CALLINGPARTYID, CIS_COMMENT, CIS_CONNECTEDIDNAME, CIS_CONNECTEDIDNUMBER, CIS_DISPLAYABLEADDRESS, CIS_REDIRECTINGIDNAME, CIS_REDIRECTINGIDNUMBER, CIS_REDIRECTIONIDNAME, CIS_REDIRECTIONIDNUMBER, _tapi3_callinfo_string, tapi3.callinfo_string, tapi3if/CALLINFO_STRING, tapi3if/CIS_CALLEDIDNAME, tapi3if/CIS_CALLEDIDNUMBER, tapi3if/CIS_CALLEDPARTYFRIENDLYNAME, tapi3if/CIS_CALLERIDNAME, tapi3if/CIS_CALLERIDNUMBER, tapi3if/CIS_CALLINGPARTYID, tapi3if/CIS_COMMENT, tapi3if/CIS_CONNECTEDIDNAME, tapi3if/CIS_CONNECTEDIDNUMBER, tapi3if/CIS_DISPLAYABLEADDRESS, tapi3if/CIS_REDIRECTINGIDNAME, tapi3if/CIS_REDIRECTINGIDNUMBER, tapi3if/CIS_REDIRECTIONIDNAME, tapi3if/CIS_REDIRECTIONIDNUMBER
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
req.typenames: CALLINFO_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLINFO_STRING
 - tapi3if/CALLINFO_STRING
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
 - CALLINFO_STRING
---

# CALLINFO_STRING enumeration


## -description

The 
<b>CALLINFO_STRING</b> enum is used by 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> methods that set and get call information involving the use of strings.

## -enum-fields

### -field CIS_CALLERIDNAME:0

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

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring">ITCallInfo::get_CallInfoString</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfostring">ITCallInfo::put_CallInfoString</a>
