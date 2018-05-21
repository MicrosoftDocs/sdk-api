---
UID: NE:roerrorapi.RO_ERROR_REPORTING_FLAGS
title: RO_ERROR_REPORTING_FLAGS
author: windows-driver-content
description: Specifies the behavior of the RoOriginateError and RoTransformError functions.
old-location: winrt\ro_error_reporting_flags.htm
old-project: WinRT
ms.assetid: 345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: RO_ERROR_REPORTING_FLAGS, RO_ERROR_REPORTING_FLAGS enumeration [Windows Runtime], RO_ERROR_REPORTING_FORCEEXCEPTIONS, RO_ERROR_REPORTING_NONE, RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS, RO_ERROR_REPORTING_SUPPRESSSETERRORINFO, RO_ERROR_REPORTING_USESETERRORINFO, roerrorapi/RO_ERROR_REPORTING_FLAGS, roerrorapi/RO_ERROR_REPORTING_FORCEEXCEPTIONS, roerrorapi/RO_ERROR_REPORTING_NONE, roerrorapi/RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS, roerrorapi/RO_ERROR_REPORTING_SUPPRESSSETERRORINFO, roerrorapi/RO_ERROR_REPORTING_USESETERRORINFO, winrt.ro_error_reporting_flags, winrt.winrterrorreportingflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	roerrorapi.h
api_name:
-	RO_ERROR_REPORTING_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RO_ERROR_REPORTING_FLAGS enumeration


## -description


Specifies the behavior of the <a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a> and <a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a> functions.


## -enum-fields




### -field RO_ERROR_REPORTING_NONE

Error functions raise structured exceptions when a debugger is attached.


### -field RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS

Error functions do not raise structured exceptions, even when a debugger is present.  Override the behavior of this flag by setting the <b>ForceExceptions</b> flag.


### -field RO_ERROR_REPORTING_FORCEEXCEPTIONS

Error functions raise structured exceptions, even if no debugger is present.  This flag supercedes the <b>RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS</b> flag.  If this flag is set, structured exceptions are raised even if the <b>RO_ERROR_REPORTING_SUPPRESSEXCEPTIONS</b> flag is set.


### -field RO_ERROR_REPORTING_USESETERRORINFO

Error functions report error strings through a COM object that is attached to the COM channel through the <a href="https://msdn.microsoft.com/3F4A62EF-ECD3-45FA-836D-77C510C43C5E">SetRestrictedErrorInfo</a> infrastructure. For the <b>SetRestrictedErrorInfo</b> call to succeed, the thread must be initialized into COM.


### -field RO_ERROR_REPORTING_SUPPRESSSETERRORINFO

Error functions do not report error strings through a COM object that is attached to the COM channel through the <a href="https://msdn.microsoft.com/3F4A62EF-ECD3-45FA-836D-77C510C43C5E">SetRestrictedErrorInfo</a> infrastructure.


## -remarks



Use the <b>RO_ERROR_REPORTING_FLAGS</b> enumeration with the <a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a> function to specify the behavior of the  <a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>, <a href="https://msdn.microsoft.com/FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B">RoOriginateErrorW</a>,  <a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a>, and <a href="https://msdn.microsoft.com/A13265FD-DC14-4552-A9FD-C954A7EA08C9">RoTransformErrorW</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/0DCF6693-5066-46E3-A7F9-5CF0780FA87C">RoGetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>



<a href="https://msdn.microsoft.com/FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B">RoOriginateErrorW</a>



<a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a>



<a href="https://msdn.microsoft.com/A13265FD-DC14-4552-A9FD-C954A7EA08C9">RoTransformErrorW</a>



<a href="https://msdn.microsoft.com/3F4A62EF-ECD3-45FA-836D-77C510C43C5E">SetRestrictedErrorInfo</a>
 

 

