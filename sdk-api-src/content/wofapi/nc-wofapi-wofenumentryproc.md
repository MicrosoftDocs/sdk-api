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

# WofEnumEntryProc callback function


## -description


Callback function that gets called for each data source in response to a call to <a href="https://msdn.microsoft.com/D6BCBFC1-C916-43E3-BB6A-E8EB6467850B">WofEnumEntries</a>.


## -parameters




### -param EntryInfo [in]

The structure that contains specific provider info. The Type of <i>EntryInfo</i> is provider-specific.  For WOF_PROVIDER_WIM,
it will be PWIM_ENTRY_INFO.



### -param UserData [in, optional]

Optional user defined data specified in the call to <a href="https://msdn.microsoft.com/D6BCBFC1-C916-43E3-BB6A-E8EB6467850B">WofEnumEntries</a>. 


## -returns



A boolean value that indicates whether the enumeration was successful. The enumeration will stop if this callback function returns FALSE.



