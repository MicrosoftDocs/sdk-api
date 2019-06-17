---
UID: NE:winevt._EVT_EXPORTLOG_FLAGS
title: EVT_EXPORTLOG_FLAGS (winevt.h)
author: windows-sdk-content
description: Defines values that indicate whether the events come from a channel or log file.
old-location: wes\evt_exportlog_flags.htm
tech.root: wes
ms.assetid: 02a63a3c-5c9b-485f-bd52-a97c40cb83d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_EXPORTLOG_FLAGS, EVT_EXPORTLOG_FLAGS enumeration [EventLog], EvtExportLogChannelPath, EvtExportLogFilePath, EvtExportLogTolerateQueryErrors, wes.evt_exportlog_flags, winevt/EVT_EXPORTLOG_FLAGS, winevt/EvtExportLogChannelPath, winevt/EvtExportLogFilePath, winevt/EvtExportLogTolerateQueryErrors
ms.topic: enum
f1_keywords: ["winevt/EVT_EXPORTLOG_FLAGS"]
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WinEvt.h
api_name:
 - EVT_EXPORTLOG_FLAGS
product: Windows
targetos: Windows
req.typenames: EVT_EXPORTLOG_FLAGS
req.redist: 
ms.custom: 19H1
---

# EVT_EXPORTLOG_FLAGS enumeration


## -description


Defines values that indicate whether the events come from a channel or log file.


## -enum-fields




### -field EvtExportLogChannelPath

The source of the events is a channel.


### -field EvtExportLogFilePath

The source of the events is a previously exported log file.


### -field EvtExportLogTolerateQueryErrors

Export events even if part of the query generates an error (is not well formed). The service validates the syntax of the XPath query to determine whether it is well formed. If the validation fails, the service parses the XPath into individual expressions. It builds a new XPath beginning with the leftmost expression. The service validates the expression and if it is valid, the service adds the next expression to the XPath. The service repeats this process until it finds the expression that is failing. It then uses the valid expressions as the XPath query (which means that you may not get the events that you expected). If no part of the XPath is valid, the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a> call fails.


### -field EvtExportLogOverwrite




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtexportlog">EvtExportLog</a>
 

 

