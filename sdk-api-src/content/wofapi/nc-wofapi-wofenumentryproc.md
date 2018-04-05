---
UID: NC:wofapi.WofEnumEntryProc
title: WofEnumEntryProc
author: windows-driver-content
description: Callback function that gets called for each data source in response to a call to WofEnumEntries.
old-location: fs\wofenumentryproc.htm
old-project: FileIO
ms.assetid: B0569A28-7B5F-451D-A972-89A6D42F9821
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*WofEnumEntryProc, *WofEnumEntryProc callback function [Files], fs.wofenumentryproc, wofapi/*WofEnumEntryProc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: WNV_REDIRECT_PARAM, *PWNV_REDIRECT_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	wofapi.h
api_name:
-	*WofEnumEntryProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofEnumEntryProc callback


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



