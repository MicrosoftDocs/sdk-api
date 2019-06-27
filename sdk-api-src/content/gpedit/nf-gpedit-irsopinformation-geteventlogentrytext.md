---
UID: NF:gpedit.IRSOPInformation.GetEventLogEntryText
title: IRSOPInformation::GetEventLogEntryText (gpedit.h)
author: windows-sdk-content
description: The GetEventLogEntryText method returns the text for a specific entry in the event log.
old-location: policy\irsopinformation_geteventlogentrytext.htm
tech.root: Policy
ms.assetid: ee408c0a-437e-4caa-90b7-9717d43e1452
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEventLogEntryText, GetEventLogEntryText method [Group Policy], GetEventLogEntryText method [Group Policy],IRSOPInformation interface, IRSOPInformation interface [Group Policy],GetEventLogEntryText method, IRSOPInformation.GetEventLogEntryText, IRSOPInformation::GetEventLogEntryText, _win32_irsopinformation_geteventlogentrytext, gpedit/IRSOPInformation::GetEventLogEntryText, policy.irsopinformation_geteventlogentrytext
ms.topic: method
f1_keywords: 
 - "gpedit/IRSOPInformation.GetEventLogEntryText"
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a> in the WMI documentation.


### -param dwEventID [in]

Specifies the event ID.


### -param ppszText [out]

Receives the pointer to a buffer containing the text of the event log entry. The calling application must free the memory allocated for this buffer with a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nn-gpedit-irsopinformation">IRSOPInformation</a>
 

 

