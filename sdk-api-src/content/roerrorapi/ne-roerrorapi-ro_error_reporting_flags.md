---
UID: NE:roerrorapi.RO_ERROR_REPORTING_FLAGS
title: RO_ERROR_REPORTING_FLAGS
description: Specifies the behavior of the RoOriginateError and RoTransformError functions.
helpviewer_keywords: ["RO_ERROR_REPORTING_FLAGS","RO_ERROR_REPORTING_FLAGS enumeration [Windows Runtime]","RO_ERROR_REPORTING_FORCEEXCEPTIONS","RO_ERROR_REPORTING_NONE","RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS","RO_ERROR_REPORTING_SUPPRESSSETERRORINFO","RO_ERROR_REPORTING_USESETERRORINFO","roerrorapi/RO_ERROR_REPORTING_FLAGS","roerrorapi/RO_ERROR_REPORTING_FORCEEXCEPTIONS","roerrorapi/RO_ERROR_REPORTING_NONE","roerrorapi/RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS","roerrorapi/RO_ERROR_REPORTING_SUPPRESSSETERRORINFO","roerrorapi/RO_ERROR_REPORTING_USESETERRORINFO","winrt.ro_error_reporting_flags","winrt.winrterrorreportingflags"]
old-location: winrt\ro_error_reporting_flags.htm
tech.root: WinRT
ms.assetid: 345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD
ms.date: 11/15/2018
ms.keywords: RO_ERROR_REPORTING_FLAGS, RO_ERROR_REPORTING_FLAGS enumeration [Windows Runtime], RO_ERROR_REPORTING_FORCEEXCEPTIONS, RO_ERROR_REPORTING_NONE, RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS, RO_ERROR_REPORTING_SUPPRESSSETERRORINFO, RO_ERROR_REPORTING_USESETERRORINFO, roerrorapi/RO_ERROR_REPORTING_FLAGS, roerrorapi/RO_ERROR_REPORTING_FORCEEXCEPTIONS, roerrorapi/RO_ERROR_REPORTING_NONE, roerrorapi/RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS, roerrorapi/RO_ERROR_REPORTING_SUPPRESSSETERRORINFO, roerrorapi/RO_ERROR_REPORTING_USESETERRORINFO, winrt.ro_error_reporting_flags, winrt.winrterrorreportingflags
f1_keywords:
- roerrorapi/RO_ERROR_REPORTING_FLAGS
dev_langs:
- c++
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
- HeaderDef
api_location:
- roerrorapi.h
api_name:
- RO_ERROR_REPORTING_FLAGS
targetos: Windows
req.typenames: RO_ERROR_REPORTING_FLAGS
req.redist: 
---

# RO_ERROR_REPORTING_FLAGS enumeration


## -description


Specifies the behavior of the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a> and <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformError</a> functions.


## -enum-fields




### -field RO_ERROR_REPORTING_NONE:0x00000000

Error functions raise structured exceptions when a debugger is attached.


### -field RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS:0x00000001

Error functions do not raise structured exceptions, even when a debugger is present.  Override the behavior of this flag by setting the <b>ForceExceptions</b> flag.


### -field RO_ERROR_REPORTING_FORCEEXCEPTIONS:0x00000002

Error functions raise structured exceptions, even if no debugger is present.  This flag supercedes the <b>RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS</b> flag.  If this flag is set, structured exceptions are raised even if the <b>RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS</b> flag is set.


### -field RO_ERROR_REPORTING_USESETERRORINFO:0x00000004

Error functions report error strings through a COM object that is attached to the COM channel through the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo">SetRestrictedErrorInfo</a> infrastructure. For the <b>SetRestrictedErrorInfo</b> call to succeed, the thread must be initialized into COM.


### -field RO_ERROR_REPORTING_SUPPRESSSETERRORINFO:0x00000008

Error functions do not report error strings through a COM object that is attached to the COM channel through the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo">SetRestrictedErrorInfo</a> infrastructure.


## -remarks



Use the <b>RO_ERROR_REPORTING_FLAGS</b> enumeration with the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a> function to specify the behavior of the  <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>, <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerrorw">RoOriginateErrorW</a>,  <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformError</a>, and <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerrorw">RoTransformErrorW</a> functions.




## -see-also




<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags">RoGetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerrorw">RoOriginateErrorW</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerrorw">RoTransformErrorW</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo">SetRestrictedErrorInfo</a>
 

 
