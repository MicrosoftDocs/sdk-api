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
 

 

