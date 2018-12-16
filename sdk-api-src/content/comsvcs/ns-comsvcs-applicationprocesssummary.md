---
UID: NS:comsvcs._ApplicationProcessSummary
title: ApplicationProcessSummary
author: windows-sdk-content
description: Represents summary information about a process hosting COM+ applications.
old-location: cos\applicationprocesssummary.htm
tech.root: cossdk
ms.assetid: 2402aca6-4992-4c6e-a6ff-b4cc50c57dde
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ApplicationProcessSummary, ApplicationProcessSummary structure [COM+], comsvcs/ApplicationProcessSummary, cos.applicationprocesssummary
ms.topic: struct
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - ComSvcs.h
api_name:
 - ApplicationProcessSummary
product: Windows
targetos: Windows
req.typenames: ApplicationProcessSummary
req.redist: 
---

# ApplicationProcessSummary structure


## -description


Represents summary information about a process hosting COM+ applications.


## -struct-fields




### -field PartitionIdPrimaryApplication

The partition ID of the COM+ server application, for server application processes. For processes that are not hosting a COM+ server application, this is set to the partition ID of the first tracked component instantiated in the process.


### -field ApplicationIdPrimaryApplication

The application ID of the COM+ server application, for server application processes. For processes that are not hosting a COM+ server application, this is set to the application ID of the first tracked component instantiated in the process.


### -field ApplicationInstanceId

The application instance GUID uniquely identifying the tracked process.


### -field ProcessId

The process ID of the tracked process.


### -field Type

The type of application this process is hosting. For COM+ server application processes, this is set to APPTYPE_SERVER. For processes that are not hosting a COM+ server applications, this is set to either APPTYPE_LIBRARY or APPTYPE_SWC, based on the first tracked component instantiated in the process.


### -field ProcessExeName

The name of the process's executable image. Space for this string is allocated by the method called and freed by the caller (for more information, see <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>). This member is not returned by default. To return this member, specify the GATD_INCLUDE_PROCESS_EXE_NAME flag when you call a method that returns an <b>ApplicationProcessSummary</b> structure.


### -field IsService

Indicates whether the process is a COM+ server application running as a Windows service.


### -field IsPaused

Indicates whether the process is a COM+ server application instance that is paused.


### -field IsRecycled

Indicates whether the process is a COM+ server application instance that has been recycled.


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

