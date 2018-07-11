---
UID: NF:gpedit.IRSOPInformation.GetEventLogEntryText
title: IRSOPInformation::GetEventLogEntryText
author: windows-sdk-content
description: The GetEventLogEntryText method returns the text for a specific entry in the event log.
old-location: policy\irsopinformation_geteventlogentrytext.htm
old-project: policy
ms.assetid: ee408c0a-437e-4caa-90b7-9717d43e1452
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: GetEventLogEntryText, GetEventLogEntryText method [Group Policy], GetEventLogEntryText method [Group Policy],IRSOPInformation interface, IRSOPInformation interface [Group Policy],GetEventLogEntryText method, IRSOPInformation.GetEventLogEntryText, IRSOPInformation::GetEventLogEntryText, _win32_irsopinformation_geteventlogentrytext, gpedit/IRSOPInformation::GetEventLogEntryText, policy.irsopinformation_geteventlogentrytext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IRSOPInformation.GetEventLogEntryText
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IRSOPInformation::GetEventLogEntryText


## -description


The
    <b>GetEventLogEntryText</b> method returns the text for a specific entry in the event log.


## -parameters




### -param pszEventSource [in]

Specifies the name of the source (application, service, driver, subsystem) that generated the log entry.


### -param pszEventLogName [in]

Specifies the name of the event log.


### -param pszEventTime [in]

Specifies the time the event was logged, in Windows Management Instrumentation (WMI) format. For more information, see 
<a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a> in the WMI documentation.


### -param dwEventID [in]

Specifies the event ID.


### -param ppszText [out]

Receives the pointer to a buffer containing the text of the event log entry. The calling application must free the memory allocated for this buffer with a call to the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/e3662977-d7a7-47bc-989b-a820d4c05382">IRSOPInformation</a>
 

 

