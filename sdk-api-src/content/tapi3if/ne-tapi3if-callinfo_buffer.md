---
UID: NE:tapi3if.CALLINFO_BUFFER
title: CALLINFO_BUFFER (tapi3if.h)
description: The CALLINFO_BUFFER enum indicates the type of buffer accessed by the ITCallInfo::GetCallInfoBuffer method or the ITCallInfo::SetCallInfoBuffer method.
helpviewer_keywords: ["CALLINFO_BUFFER","CALLINFO_BUFFER enumeration [TAPI 2.2]","CIB_CALLDATABUFFER","CIB_CHARGINGINFOBUFFER","CIB_DEVSPECIFICBUFFER","CIB_HIGHLEVELCOMPATIBILITYBUFFER","CIB_LOWLEVELCOMPATIBILITYBUFFER","CIB_USERUSERINFO","_tapi3_callinfo_buffer","tapi3.callinfo_buffer","tapi3if/CALLINFO_BUFFER","tapi3if/CIB_CALLDATABUFFER","tapi3if/CIB_CHARGINGINFOBUFFER","tapi3if/CIB_DEVSPECIFICBUFFER","tapi3if/CIB_HIGHLEVELCOMPATIBILITYBUFFER","tapi3if/CIB_LOWLEVELCOMPATIBILITYBUFFER","tapi3if/CIB_USERUSERINFO"]
old-location: tapi3\callinfo_buffer.htm
tech.root: tapi3
ms.assetid: 76774741-2aa3-455c-a203-1daee42cf0fa
ms.date: 12/05/2018
ms.keywords: CALLINFO_BUFFER, CALLINFO_BUFFER enumeration [TAPI 2.2], CIB_CALLDATABUFFER, CIB_CHARGINGINFOBUFFER, CIB_DEVSPECIFICBUFFER, CIB_HIGHLEVELCOMPATIBILITYBUFFER, CIB_LOWLEVELCOMPATIBILITYBUFFER, CIB_USERUSERINFO, _tapi3_callinfo_buffer, tapi3.callinfo_buffer, tapi3if/CALLINFO_BUFFER, tapi3if/CIB_CALLDATABUFFER, tapi3if/CIB_CHARGINGINFOBUFFER, tapi3if/CIB_DEVSPECIFICBUFFER, tapi3if/CIB_HIGHLEVELCOMPATIBILITYBUFFER, tapi3if/CIB_LOWLEVELCOMPATIBILITYBUFFER, tapi3if/CIB_USERUSERINFO
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
req.typenames: CALLINFO_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLINFO_BUFFER
 - tapi3if/CALLINFO_BUFFER
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
 - CALLINFO_BUFFER
---

# CALLINFO_BUFFER enumeration


## -description

The 
<b>CALLINFO_BUFFER</b> enum indicates the type of buffer accessed by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">ITCallInfo::GetCallInfoBuffer</a> method or the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">ITCallInfo::SetCallInfoBuffer</a> method.

The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">ITCallInfo::get_CallInfoBuffer</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">ITCallInfo::put_CallInfoBuffer</a> methods are provided for Automation client applications, such as those written in Visual Basic.

## -enum-fields

### -field CIB_USERUSERINFO:0

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

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">ITCallInfo::GetCallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">ITCallInfo::SetCallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">ITCallInfo::get_CallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">ITCallInfo::put_CallInfoBuffer</a>
