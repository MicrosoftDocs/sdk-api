---
UID: NF:winevt.EvtOpenLog
title: EvtOpenLog function
author: windows-sdk-content
description: Gets a handle to a channel or log file that you can then use to get information about the channel or log file.
old-location: wes\evtopenlog.htm
old-project: WES
ms.assetid: 1bf81452-2a62-4999-91b1-f1b42e6db91f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EvtOpenLog, EvtOpenLog function [EventLog], wes.evtopenlog, winevt/EvtOpenLog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winevt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtOpenLog
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtOpenLog function


## -description


Gets a handle to a channel or log file that you can then use to get information about the channel or log file.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to open a channel or log on the local computer.


### -param Path [in]

The name of the channel or the full path to the exported log file.


### -param Flags [in]

A flag that determines whether the <i>Path</i> parameter points to a log file or channel. For possible values, see the <a href="https://msdn.microsoft.com/c5badaee-4b3b-448a-9a91-df58be1ec884">EVT_OPEN_LOG_FLAGS</a> enumeration.


## -returns



If successful, the function returns a handle to the file or channel; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



Relative paths and environment variables cannot be used when specifying a file.  A Universal Naming Convention (UNC) path can be used to locate the file.  Any relative path and environment variable expansion needs to be done prior to making API calls.

To get information about the channel or log file, call the <a href="https://msdn.microsoft.com/5261f367-3010-4b6d-9a53-77c908c867d4">EvtGetLogInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a>



<a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a>



<a href="https://msdn.microsoft.com/5261f367-3010-4b6d-9a53-77c908c867d4">EvtGetLogInfo</a>
 

 

