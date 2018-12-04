---
UID: NF:winevt.EvtOpenEventMetadataEnum
title: EvtOpenEventMetadataEnum function
author: windows-sdk-content
description: Gets a handle that you use to enumerate the list of events that the provider defines.
old-location: wes\evtopeneventmetadataenum.htm
tech.root: wes
ms.assetid: e1d2e5d5-89db-4bda-9803-37f26d1fe30f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EvtOpenEventMetadataEnum, EvtOpenEventMetadataEnum function [EventLog], wes.evtopeneventmetadataenum, winevt/EvtOpenEventMetadataEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtOpenEventMetadataEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtOpenEventMetadataEnum function


## -description


Gets a handle that you use to enumerate the list of events that the provider defines.


## -parameters




### -param PublisherMetadata [in]

A handle to the provider's metadata that the <a href="https://msdn.microsoft.com/0839fb15-12a9-4e30-9afa-6f6437956df0">EvtOpenPublisherMetadata</a> function returns.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the list of events that the  provider defines; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



To enumerate the events, call the <a href="https://msdn.microsoft.com/1077dc7c-3e73-4135-9020-20d086e30e71">EvtNextEventMetadata</a> function in a loop.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a>



<a href="https://msdn.microsoft.com/1077dc7c-3e73-4135-9020-20d086e30e71">EvtNextEventMetadata</a>
 

 

