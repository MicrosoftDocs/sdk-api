---
UID: NS:comsvcs._ApplicationProcessSummary
title: ApplicationProcessSummary (comsvcs.h)
description: Represents summary information about a process hosting COM+ applications.
helpviewer_keywords: ["ApplicationProcessSummary","ApplicationProcessSummary structure [COM+]","comsvcs/ApplicationProcessSummary","cos.applicationprocesssummary"]
old-location: cos\applicationprocesssummary.htm
tech.root: cos
ms.assetid: 2402aca6-4992-4c6e-a6ff-b4cc50c57dde
ms.date: 12/05/2018
ms.keywords: ApplicationProcessSummary, ApplicationProcessSummary structure [COM+], comsvcs/ApplicationProcessSummary, cos.applicationprocesssummary
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
targetos: Windows
req.typenames: ApplicationProcessSummary
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ApplicationProcessSummary
 - comsvcs/_ApplicationProcessSummary
 - ApplicationProcessSummary
 - comsvcs/ApplicationProcessSummary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ApplicationProcessSummary
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

The name of the process's executable image. Space for this string is allocated by the method called and freed by the caller (for more information, see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>). This member is not returned by default. To return this member, specify the GATD_INCLUDE_PROCESS_EXE_NAME flag when you call a method that returns an <b>ApplicationProcessSummary</b> structure.

### -field IsService

Indicates whether the process is a COM+ server application running as a Windows service.

### -field IsPaused

Indicates whether the process is a COM+ server application instance that is paused.

### -field IsRecycled

Indicates whether the process is a COM+ server application instance that has been recycled.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>