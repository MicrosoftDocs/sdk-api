---
UID: NS:processthreadsapi._APP_MEMORY_INFORMATION
title: APP_MEMORY_INFORMATION (processthreadsapi.h)
author: windows-sdk-content
description: Represents app memory usage at a single point in time. This structure is used by the PROCESS_INFORMATION_CLASS class.
old-location: base\app_memory_information.htm
tech.root: ProcThread
ms.assetid: A2D0CDED-0E8B-41D6-8435-BDB4E5445DE4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PAPP_MEMORY_INFORMATION, APP_MEMORY_INFORMATION, APP_MEMORY_INFORMATION structure, PAPP_MEMORY_INFORMATION, PAPP_MEMORY_INFORMATION structure pointer, base.app_memory_information, processthreadsapi/APP_MEMORY_INFORMATION, processthreadsapi/PAPP_MEMORY_INFORMATION"
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - processthreadsapi.h
api_name:
 - APP_MEMORY_INFORMATION
product: Windows
targetos: Windows
req.typenames: APP_MEMORY_INFORMATION, *PAPP_MEMORY_INFORMATION
req.redist: 
ms.custom: 19H1
---

# APP_MEMORY_INFORMATION structure


## -description


Represents app memory usage at a single point in time. This structure is used by the <a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS</a> class.


## -struct-fields




### -field AvailableCommit

Total commit available to the app.


### -field PrivateCommitUsage

The app's usage of private commit.


### -field PeakPrivateCommitUsage

The app's peak usage of private commit.


### -field TotalCommitUsage

The app's total usage of private plus shared commit.


## -see-also




<a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS</a>
 

 

